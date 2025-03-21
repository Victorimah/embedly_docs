# Search Wallet by Email

The `GET /api/v1/wallets/search/email` endpoint allows you to search for a wallet associated with a specified email address.

## Request

### **URL**

`https://api/v1/wallets/search/email`

### **Query Parameters**

| Parameter     | Type   | Description                               |
|---------------|--------|-------------------------------------------|
| `email`       | string | Email address to search for (required).  |

## Response

``` json
✅ Success Response

Status Code: 200 OK

{
  "code": "200",
  "success": true,
  "message": "Wallet found.",
  "data": {
    // Details of the wallet associated with the email
  }

  ```

## ❌ Error Responses

Status Code: 400 Bad Request

``` json
{
  "code": "400",
  "success": false,
  "message": "Invalid request data",
  "data": null
}

Status Code: 500 Internal Server Error

{
  "code": "500",
  "success": false,
  "message": "The key value at position 0 of the call to 'DbSet<VirtualAccountProvider>.Find' was of type 'int', which does not match the property type of 'Guid'.",
  "data": null
}
