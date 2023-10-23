# Location APIs

## Get Last Scanned Location and Timestamp

**URL:** https://app.tec-rfid.co.uk/api/last-scanned-location-and-timestamp

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

```

  {
    "api_key": "APIKEY",
    "asset_tag": "EPC/RFIDCODE"
  }

```

**Sample Response:**

```

  {
    "status": "success",
    "message": "",
    "data": {
      "asset_tag": "0088881000010000",
      "last_scanned_location": "Test Location 1",
      "timestamp_last_scan": "15/04/2023 17:52:11"
    }
  }

```

## Get Last X Amount of Scanned Locations

**URL:** https://app.tec-rfid.co.uk/api/last-x-amount-of-scanned-locations

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

```

  {
    "api_key": "APIKEY",
    "asset_tag": "TAG/EPC/RFIDCODE",
    "no_of_locations": INTEGER
  }

```

**Sample Response:**

```

  {
    "status": "success",
    "message": "",
    "data": [
      {
        "location": "Location A",
        "first_scan": "14/02/2023 17:52:11",
        "last_scan": "01/05/2023 17:52:11"
      },
      {
        "location": "Location B",
        "first_scan": "22/03/2023 17:52:11",
        "last_scan": "29/04/2023 17:52:11"
      }
    ]
  }

```

## Items Seen at Location in Last X Seconds

**URL:** https://app.tec-rfid.co.uk/api/item-seen-at-location-in-last-x-seconds

**Method:** POST

**Headers:** 
 - Content-Type: application/json

**Payload Format:**

```

  {
    "api_key": "APIKEY",
    "location": "LOCATION_NAME",
    "seconds": INTEGER
  }

```

**Sample Response:**

```

  {
   "status": "success",
   "message": "",
   "data": {
     "assets": [
       {
         "id": 76,
         "name": "Testing Asset 2 (Dell 431)",
         "asset_tag": "EPC00000002",
         "asset_number": null,
         "image": null,
         "serial_number": "12345",
         "description": "This is just for testing 2",
         "due_date": "16/06/2022",
         "category": "Electronics.",
         "user": "New Test User 1",
         "location": "Liverpool",
         "value": "200000",
         "notes": "Testing Note",
         "asset_type": "LED",
         "last_scan_timestamp": "16/04/2023 17:52:11"
       },
       {
         "id": 76,
         "name": "Testing Asset 2 (Dell 431)",
         "asset_tag": "EPC00000002",
         "asset_number": null,
         "image": null,
         "serial_number": "12345",
         "description": "This is just for testing 2",
         "due_date": "16/06/2022",
         "category": "Electronics.",
         "user": "New Test User 1",
         "location": "Liverpool",
         "value": "200000",
         "notes": "Testing Note",
         "asset_type": "LED",
         "last_scan_timestamp": "16/04/2023 17:52:11"
       }
     ]
   }
  }

```
