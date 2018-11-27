# Calling Azure Functions locally

## TYPE

```http
POST
```

## URL

```http
http://localhost:7071/api/Translate
```

## Body

```json
{
   "values": [
        {
            "recordId": "a1",
            "data":
            {
               "text":  "Esta es una excelente presentacion"
            }
        }
   ]
}
```
