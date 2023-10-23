# Create Assets API

## Create Asset

**URL:** https://app.tec-rfid.co.uk/api/create-asset-api

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

The required payload will vary significantly depending on your organisation's required fields. To determine your required format, just send your API key on its own, as below, and the response will be reference JSON for you to use. 

```
  {
    "api_key": "APIKEY"
  }
```

**Response Types:**

*Success*

```

 {
    "status": "success",
    "message": "Asset created successfully",
    "data": [
       {RETURNS JSON OBJECT FOR ASSET CREATED}
    ]
 }

```

*Failure*

```

 {
    "status": "fail",
    "message": "Please use following format",
    "JsonBodyFormat": {REFERENCE FORMAT FOR YOUR ORGANISATION}
 }

```

## Bulk Create Assets

**URL:** https://app.tec-rfid.co.uk/api/v3/create-bulk-asset-api

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

Identical to above, the one difference being that you nest the assets inside an array, like so: 

```
  {
    "api_key": "APIKEY",
    "assets": [
      {ONE JSON OBJECT FOR EACH ASSET TO BE CREATED}
    ]
  }
```
