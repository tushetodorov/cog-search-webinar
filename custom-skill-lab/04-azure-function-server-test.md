# Calling Azure Functions on Azure, after publishing the code

## TYPE

```http
POST
```

## URL

```http
https://your-function-name-here.azurewebsites.net/api/Translate?code=your-azure-functions-key-here
```

## Header

```http
Content-Type : application/json
```


## Body

```json
{
   "values": [
        {
            "recordId": "a1",
            "data":
            {
               "text":  "Mi gato persigue a mi perro."
            }
        }
   ]
}
```
