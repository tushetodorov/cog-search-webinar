# Creating a Data Source

## Type

```http
POST
```

## URL

```http
https://your-azure-search-service-name.search.windows.net/datasources?api-version=2017-11-11-Preview
```

## Headers

```http
Content-Type : application/json
api-key : your-azure-search-key
```

## Body
```json
{   
    "name" : "newdatasource",  
    "description" : "Demo files to demonstrate cognitive search capabilities.",  
    "type" : "azureblob",
    "credentials" :
    { "connectionString" :
      "DefaultEndpointsProtocol=https;AccountName=mystorageaccountrod;AccountKey=z/VnjtyHpVwsrwLfGw9ADPmGIP9bk7EW6yp3ozVwu+XOjBbD41CrUuVpQvoKYHYdI0uljDXNGLTSSV/VUID4PA==;EndpointSuffix=core.windows.net"
    },  
    "container" : { "name" : "dataset" }
}  
```
