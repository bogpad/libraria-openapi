# Query Library
<code>POST<code> <code>/library/:library_id/query<code>

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
| :query | string | |
| :conversation_id (optional) | string | Keeps the conversation history for chat |

<br/>

### Sample Body
```json
{
  "query": "What is the capital of France?",
  "conversation_id": "optional-unique-id"
}
```

### Sample Response
```json
{
  "reply": "The capital of France is Paris.",
  "conversation_id": "unique_id"
}
```

<br/>

### Sample CURL
```
curl -X POST \\
  https://api.libraria.dev/library/:library_id/query \\
  -H 'Content-Type: application/json' \\
  -H 'x-api-key: <YOUR_API_KEY>' \\
  -d '{
    "query": "What is the capital of France?",
    "conversation_id": "optional-unique-id"
  }
```

<br/>

### Sample axios
```javascript
axios.post('https://api.libraria.dev/library/:library_id/query', {
  query: "What is the capital of France?",
  conversation_id: "optional-unique-id",
}, {
  headers: {
    'x-api-key': <YOUR_API_KEY>
  }
})
```
