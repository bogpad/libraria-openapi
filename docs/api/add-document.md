# Add Document to Library
<code>POST<code> <code>/library/:library_id/document<code>

<br/>

### Requirements
| ||
|------|-----|
| API Key | { headers: { x-api-key: "<YOUR_API_KEY>" } } |

<br/>

### Path Parameters
| ||
|------|-----|
| :library_id |string  |

<br/>


### Request body
|  |  |   |
|------|-----|-----|
| :url | string[] | |

<br/>

### Sample Body
```json
{
  "urls": [
    "https://example.com/article1",
    "https://example.com/article2"
  ]
}
```

### Sample Response
```json
{
  "status": "queued",
  "message": "URLs queued for processing"
}
```

<br/>

### Sample CURL
```
curl -X POST \\
  https://api.libraria.dev/library/1 \\
  -H 'Content-Type: application/json' \\
  -H 'x-api-key: <YOUR_API_KEY>' \\
  -d '{
    "urls": [
      "https://example.com/article1",
      "https://example.com/article2"
    ]
  }
```

<br/>

### Sample axios
```javascript
axios.post('https://api.libraria.dev/library/:library_id/document', {
  urls: [
    "https://example.com/article1",
    "https://example.com/article2"
  ]
}, {
  headers: {
    'x-api-key': <YOUR_API_KEY>
  }
})
```
