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
    "name" : "recipes",  
    "description" : "Demo files to demonstrate cognitive search capabilities.",  
    "type" : "azureblob",
    "credentials" :
    { "connectionString" :       "your-connection-string-here"    },  
    "container" : { "name" : "your-container-name-here" }
}  
```
