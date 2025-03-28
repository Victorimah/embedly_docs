# Get Account Closure Reasons API

The `GET /api/v1/wallets/account/closure/reasons` endpoint retrieves the reasons available for closing an account.

### **URL**

`https://api/v1/wallets/account/closure/reasons`

## Request

`GET`

## Response

✅ Success Response

```json

Status Code: 200 OK

{
  "code": "200",
  "success": true,
  "message": "Account closure reasons retrieved successfully.",
  "data": [
    {
      "id": 1,
      "reason": "No longer needed"
    },
    {
      "id": 2,
      "reason": "Moving to a different bank"
    }
    // Additional reasons may be listed
  ]
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
  "message": "PROCEDURE bankify GET_ACCOUNT_CLOSURE_REASONS does not exist",
  "data": null
}
