# Fixed Reader API

## Adding/Updating Reader IDs

On the web portal, go to Locations, find the location you're looking for, and click Edit (pencil icon). The Reader Id(s) field is towards the bottom of the Edit interface. Reader IDs must be alphanumeric; you can add multiple reader IDs, comma-separated.

![updating reader ID](https://github.com/TEC-RFID/rfid-asset-documentation/blob/main/images/setreaderid.gif?raw=true)

## Update Asset Location By Reader ID

**URL:** https://app.tec-rfid.co.uk/api/update-asset-location-by-reader-id

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

```
  {
    "api_key": "API_KEY",
    "reader_id": "READER_ID",
    "tag": "EPC (RFIDCODE)"
  }
```

**Example Payload:**

```
  {
    "api_key": "cxVYOm3Kqy1hFHGydatCIKoZY2AtffS3hO0JeZly",
    "reader_id": "RED31",
    "tag": "EPC00000001"
  }
```

**Response Types:**

*Success*

```
  {
    "status": "success",
    "message": "asset updated successfully"
  }
```

*Failure*

```
  {
    "status": "fail",
    "message": "reader not found"
  }
  {
    "status": "fail",
    "message": "asset not found"
  }
  {
    "status": "fail",
    "message": "API Key is missing."
  }
  {
    "status": "fail",
    "message": "Invalid API Key."
  }
```

## Bulk Update Asset Location By Reader ID

**URL:** https://app.tec-rfid.co.uk/api/bulk-update-asset-location-by-reader

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

```
  {
    "api_key": "API_KEY",
    "data": [
      {"reader_id":"READER_ID","tag":"EPC (RFIDCODE)","timestamp":"DATETIME"}
    ]
  }
```

**Example Payload:**

```
  {
    "api_key": "cxVYOm3Kqy1hFHGydatCIKoZY2AtffS3hO0JeZly",
    "data":[
      {"reader_id":"r2", "tag": "aaa2", "timestamp":"2023-06-11 11:37:42"},
      {"reader_id":"r2", "tag": "aaa3", "timestamp":"2023-06-11 11:36:42"}
    ]  
  }
```

**Response Types:**

*Success*

```
  {
    "status": "success",
    "message": "locations updated successfully",
    "processing_time": 0
  }
```

*Failure*

```
  {
    "status": "fail",
    "message": "Something went wrong when loading your data"
  }
```
