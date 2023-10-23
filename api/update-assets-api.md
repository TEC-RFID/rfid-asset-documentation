# Update Assets API

## Update Asset

**URL:** https://app.tec-rfid.co.uk/api/update-asset-api

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

You will only need to send required fields (which will always include asset ID, name, and tag, but are otherwise determined by your organization's settings). Fields sent with null or blank values in the payload will be overwritten; if you want a field to retain its original value, don't send it in the payload and it will be ignored. Since you will need to include required fields even if you don't want to change them, we suggest structuring your code to make sure you have access to and are sending all required fields in your API updates. 

**Response Types:**

*Success*

```

 {
    "status": "success",
    "message": "Asset updated successfully",
    "data": [
       {RETURNS JSON OBJECT FOR ASSET UPDATED}
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
