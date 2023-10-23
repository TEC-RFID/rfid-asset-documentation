# Get Assets API

## Get All Assets with Filters

**URL:** https://app.tec-rfid.co.uk/api/get-all-assets-with-filters

This will return all assets that match the search criteria. If you want to use pagination (30 results per page), append ?page=PAGENUMBER to the URL. 

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

```
  {
    "api_key": "APIKEY",
    "created_at_range": "01/01/2023,20/05/2023"
    "rfid_code": "EPC",
    "asset_name": "ASSETNAME",
    "asset_type": "ASSETTYPE",
    "category": "CATEGORY",
    "location": "LOCATION",
    "user": "USER",
    "asset_group": "ASSETGROUP",
    "status": "STATUS"
  }
```

**Notes:**
 - All filters are optional (with the obvious exception of api_key), so you can filter as much or as little as you need. 
 - created_at_range should be dd/mm/yyyy, comma separated. 
 - If no results are found, it'll still return a success response, but "data" will equal null instead of an array.
 - If pagination is not used, the "pagination" key will still be present in the response, but it will equal null. 

**Response Types:**

*Success*

```

 {
    "status": true,
    "message": "Filtered Results",
    "data": [
       {RETURNS JSON OBJECT FOR EACH ASSET FOUND}
    ],
    "pagination": {
        "current_page": 1,
        "max_pages": 0,
        "row_per_page": 30
    }
 }

```

*Failure*

```

 {
    "status": "fail",
    "message": "Invalid API Key.",
    "data": []
 }

```
