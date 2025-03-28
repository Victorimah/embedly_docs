# Wallet History API

## Overview  

The `POST /api/v1/wallets/history` endpoint displays the transaction history for a specific wallet within an organization over a specified time range.

### URL

`POST https://waas-staging.cafeone.ng/api/v1/wallets/history`

### **Request Body**  

```json
{
  "customerId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "organizationId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "walletId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "from": "2025-03-19T16:18:37.676Z",
  "to": "2025-03-19T16:18:37.676Z"
}
```

## Response

✅ Success Response
Status Code: `200 OK`

```json
{
    "success": true,
    "status": "success",
    "data": {
             "id": 1,
            "name": "John Doe",
            "email": "john.doe@example.com"
    },
    "timestamp": "2023-09-20T14:30:45Z"
}
```

### ❌ Error Responses

Status Code Error Type Description

```json
400 Bad Request Invalid Request If the request body is invalid or missing required fields.
404 Not Found Wallet Not Found If the specified wallet does not exist in the system.
500 Internal Server Error Server Error If there is an unexpected issue on the server.

{
  "code": "404",
  "success": false,
  "message": "Wallet not found",
  "data": null
}
```
