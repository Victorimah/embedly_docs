# Wallet Add API

## Overview

The `POST /api/v1/wallets/add` API endpoint is designed to create a new wallet for a customer. This wallet can be used for various transactions, tracking balances, and managing funds associated with a specific customer account.

## Request

### HTTP Method

`POST`

### Endpoint

`/api/v1/wallets/add`

### Request Headers

- **Content-Type**: `application/json`

### Request Body

The request body should be in JSON format and include the following parameters:

```json
{
  "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "walletGroupId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "customerId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "availableBalance": 23444440,
  "ledgerBalance": 500000,
  "walletRestrictionId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "walletClassificationId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "currencyId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "isInternal": true,
  "isDefault": true,
  "name": "Emmanuel Imah",
  "overdraft": 0,
  "virtualAccount": {
    "accountNumber": "0330000045",
    "bankCode": "504",
    "bankName": "Union"
  },
  "mobNum": "2345678880",
  "customerTypeId": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
}
```

## Response

✅ Success Response

Status Code: `201 Created`
Response Body:  

```json
{
  "message": "Wallet created successfully.",
  "walletId": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
}
```
