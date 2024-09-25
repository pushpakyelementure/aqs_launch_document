
COMMUNITY APIs

1.  ADD COMMUNITY

API: POST method

Endpoint = `api/v1/community/`

Purpose: This endpoint create a new community information to the database

Flowchat: 

Request:
```json
    {
        "community_name": "string",
        "location": {
          "address": "string",
          "city": "string",
          "state": "string",
          "country": "string",
          "zip_code": "string",
          "time_zone": "string"
        },
        "dwelling_types": [
          {}
        ],
        "bill_model": "string",
        "billing_cycle_date": 0,
        "billing_start_date": "2024-09-19T11:26:50.600Z",
        "next_invoice_date": "2024-09-19T11:26:50.600Z",
        "gst_no": "string",
        "subscription_status": "active"
    }       
```
Response:
```json
    {
        "community_id": "string",
        "detail": "string"
    }
```

2. GET COMMUNITY

API: GET method

Endpoint = `api/v1/community/{community_id}`

Purpose: This endpoint Read a community details from database by using community_id

Flowchat: 

Path Parameter:

    community_id: The UUID of the read a community the data.

Request:

```json
None
```

Response:
```json
    {
        "community_name": "string",
        "location": {
          "address": "string",
          "city": "string",
          "state": "string",
          "country": "string",
          "zip_code": "string",
          "time_zone": "string"
        },
        "dwelling_types": [
          {}
        ],
        "bill_model": "string",
        "billing_cycle_date": 0,
        "billing_start_date": "2024-09-19T11:29:12.950Z",
        "next_invoice_date": "2024-09-19T11:29:12.950Z",
        "gst_no": "string",
        "subscription_status": "active",
        "meta": {
          "ver": 0,
          "created_by": "string",
          "created_at": "2024-09-19T11:29:12.950Z",
          "activity": {
            "updated_by": "string",
            "updated_at": "2024-09-19T11:29:12.950Z"
          }
        }
    }
```

3. GET ALL COMMUNITY

API: GET method

Endpoint = `api/v1/community`

Purpose: This endpoint Read all community details from database.

Flowchat: 

Path Parameter:

    community_id: The UUID of the particular community to read all community from the database.

Request:

```json
None
```

Response:
```json    
    [      
        {
            "community_name": "string",
            "location": {
            "address": "string",
            "city": "string",
            "state": "string",
            "country": "string",
            "zip_code": "string",
            "time_zone": "string"
            },
            "dwelling_types": [
              {}
            ],
            "bill_model": "string",
            "billing_cycle_date": 0,
            "billing_start_date": "2024-09-19T11:29:12.950Z",
            "next_invoice_date": "2024-09-19T11:29:12.950Z",
            "gst_no": "string",
            "subscription_status": "active",
            "meta": {
              "ver": 0,
              "created_by": "string",
              "created_at": "2024-09-19T11:29:12.950Z",
              "activity": {
                "updated_by": "string",
                "updated_at": "2024-09-19T11:29:12.950Z"
              }
            }
        }
    ]
```

4. UPDATE COMMUNITY

API: PUT method

Endpoint = `api/v1/community/{community_id}`

Purpose: This endpoint update the community information by using community_id


Flowchat: 

Path Parameter:

    community_id: The UUID of the particular community to update community data.

Request:
```json
    {
        "community_name": "string",
        "location": {
          "address": "string",
          "city": "string",
          "state": "string",
          "country": "string",
          "zip_code": "string",
          "time_zone": "string"
        },
        "dwelling_types": [
          {}
        ],
        "bill_model": "string",
        "billing_cycle_date": 0,
        "billing_start_date": "2024-09-19T11:31:36.698Z",
        "next_invoice_date": "2024-09-19T11:31:36.698Z",
        "gst_no": "string",
        "subscription_status": "active"
    }

```
Response:
```json
    {
        "community_name": "string",
        "location": {
        "address": "string",
        "city": "string",
        "state": "string",
        "country": "string",
        "zip_code": "string",
        "time_zone": "string"
        },
        "dwelling_types": [
          {}
        ],
        "bill_model": "string",
        "billing_cycle_date": 0,
        "billing_start_date": "2024-09-19T11:31:36.701Z",
        "next_invoice_date": "2024-09-19T11:31:36.701Z",
        "gst_no": "string",
        "subscription_status": "active",
        "meta": {
          "ver": 0,
          "activity": {
            "updated_by": "string",
            "updated_at": "2024-09-19T11:31:36.701Z"
          }
        }
    }
```

5. CHANGE THE SUBSCRIPTIONS STATUS FOR PARTICULAR COMMUNITY

API: PATCH method

Endpoint = `api/v1/community/{community_id}`

Purpose: This endpoint update the subscription status by using community_id

Flowchat: 

Path Parameter:

    community_id: The UUID of the community to update community subscription status.

Request:
```json
    {
        "subscription_status": "active"
    }

```
Response:
```json
    {
        "detail": "string",
        "subscription_status": "active",
        "meta": {
            "ver": 0,
            "activity": {
                "updated_by": "string",
                "updated_at": "2024-09-19T11:39:50.335Z"
          }
        }
}
```
6. DELETE COMMUNITY

API: DELETE method

Endpoint = `api/v1/community/{community_id}`

Purpose: This endpoint delete the community from database by using community_id.

Flowchat: 

Path Parameter:

    community_id: The UUID of the particular community to delete community data.

Request:

```json
None
```

Response:

```json
    NULL
```