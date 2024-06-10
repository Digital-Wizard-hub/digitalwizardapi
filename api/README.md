# API documentation

Version: `v1`

## Table of Contents

- [Products `v1`](products/v1/README.md)
- [Products `v2`](products/v2/README.md)
- [Orders `v1`](order/v1/README.md)
- [Orders `v2`](order/v2/README.md)
- [Balance](balance/v1/README.md)
- [Errors Codes](ErrorsCodes.md)

## Environment

**PRODUCTION API**: https://api2.digitalwizard.com/integration or https://gateway.digitalwizard.com/esa/api (recommended)

> The `https://api2.digitalwizard.com/integration/v1` will be removed at the end of the 2020.

**SANDBOX API**: https://gateway.sandbox.digitalwizard.com/esa/api

## How to create SANDBOX account

You can create SANDBOX account [here](https://sandbox.digitalwizard.com/integration) and get the API key analogical as on production. See [Quick start](../quickstart/README.md). 

After that, ask your business manager to fill your account with balance.

## Authorization

Authorization is based on HTTP header `X-Api-Key`. You can find your API key in a Dashboard in **MY STORES** section.

### Example

```bash
curl -X POST
     -H 'X-Api-Key: [api-key]' \
     https://gateway.digitalwizard.com/esa/api/v1/products
```

> Remember that credentials on SANDBOX environment are different.

If invalid API key is being provided you can expect response in below format:

```json
{
  "kind": "Authorization",
  "status": 401,
  "detail": "Invalid authentication data.",
  "type": "Unauthorized"
}
```
