DWELLING APIs

1.  ADD DWELLING

API: POST method

Endpoint = `api/v1/dwelling/community/{community_id}`

Purpose: This endpoint create a new dwelling information to the database

Flowchat: 
![image](./admin_flowchat/admin_create.png)

Request:
```json
    {
        "block": "string",
        "floor_no": "string",
        "flat_no": "string",
        "type_of": "string"
    }

```
Response:
```json
    {
        "dwelling_id": "string",
        "detail": "string"
    }
```

2. GET DWELLING

API: GET method

Endpoint = `api/v1/dwelling/{dwelling_id}`

Purpose: This endpoint Read a dwelling details from database by using dwelling_id

Flowchat: 

Path Parameter:

    dwelling_id: The UUID of the read a dwelling the data.

Request:

```json
None
```

Response:
```json
    {
        "community_id": "string",
        "dwelling_id": "string",
        "community_name": "string",
        "block": "string",
        "floor_no": "string",
        "flat_no": "string",
        "type_of": "string",
        "time_zone": "string",
        "devices": [
          {
            "device_id": "string",
            "device_type": "water_measure_mechanical",
            "serial_no": "string",
            "group": "string",
            "tag": "string",
            "customTag": [
              "string"
            ],
            "status": "active"
          }
        ],
        "meta": {
            "ver": 0,
            "created_by": "string",
            "created_at": "2024-09-23T06:12:42.496Z",
            "activity": {
                "updated_by": "string",
                "updated_at": "2024-09-23T06:12:42.496Z"
            }
        }
    }
```

3. GET ALL DWELLING

API: GET method

Endpoint = `api/v1/dwelling/community/{community_id}`

Purpose: This endpoint Read all dwelling details from database.

Flowchat: 

Path Parameter:

    community_id: The UUID of the particular community to read all dwelling from the database.

Request:

```json
None
```

Response:
```json    
    [
        {
            "community_id": "string",
            "dwelling_id": "string",
            "community_name": "string",
            "block": "string",
            "floor_no": "string",
            "flat_no": "string",
            "type_of": "string",
            "time_zone": "string",
            "devices": [
              {
                "device_id": "string",
                "device_type": "water_measure_mechanical",
                "serial_no": "string",
                "group": "string",
                "tag": "string",
                "customTag": [
                  "string"
                ],
                "status": "active"
              }
            ]
        }
    ]
```

4. UPDATE DWELLING

API: PATCH method

Endpoint = `api/v1/dwelling/{dwelling_id}}`

Purpose: This endpoint update the dwelling information by using dwelling_id


Flowchat: 

Path Parameter:

    dwelling_id: The UUID of the particular dwelling to update dwelling data.

Request:

```json
    {
      "block": "string",
      "floor_no": "string",
      "flat_no": "string",
      "type_of": "string"
    }
```

Response:
```json
    {
        "community_id": "string",
        "dwelling_id": "string",
        "community_name": "string",
        "block": "string",
        "floor_no": "string",
        "flat_no": "string",
        "type_of": "string",
        "time_zone": "string",
        "devices": [
          {
            "device_id": "string",
            "device_type": "water_measure_mechanical",
            "serial_no": "string",
            "group": "string",
            "tag": "string",
            "customTag": [
              "string"
            ],
            "status": "active"
          }
        ],
        "meta": {
          "ver": 0,
          "created_by": "string",
          "created_at": "2024-09-23T06:16:29.482Z",
          "activity": {
            "updated_by": "string",
            "updated_at": "2024-09-23T06:16:29.482Z"
          }
        }
    }       
```

5. DELETE DWELLING 

API: DELETE method

Endpoint = `api/v1/dwelling/{dwelling_id}`

Purpose: This endpoint delete the dwelling from database by using dwelling_id.

Flowchat: 

Path Parameter:

    dwelling_id: The UUID of the particular dwelling to delete dwelling data.

Request:

```json
None
```

Response:

```json
    NULL
```