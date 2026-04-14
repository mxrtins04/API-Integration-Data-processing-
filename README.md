# Gender Classification API

A REST API that classifies the gender of a name using the Genderize.io API, with data processing and confidence scoring.

## Endpoint

**GET** `/api/classify?name={name}`

### Success Response
```json
{
  "status": "success",
  "data": {
    "name": "Martins",
    "gender": "male",
    "probability": 0.89,
    "sample_size": 11480,
    "is_confident": true,
    "processed_at": "2026-04-14T01:18:27Z"
  }
}
```

### Error Response
```json
{
  "status": "error",
  "message": "<error message>"
}
```

### Status Codes
| Code | Reason |
|------|--------|
| 200 | Success |
| 400 | Missing or empty name parameter |
| 422 | Name contains non-alphabet characters |
| 502 | Genderize API unreachable |
| 500 | Unexpected server error |

## Live API

```
https://api-integration-data-processing-production-c2d7.up.railway.app
```
