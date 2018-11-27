# Creating an Indexer

## Type

```http
PUT
```

## URL

```http
https://your-azure-search-service-name.search.windows.net/indexers/newindexer?api-version=2017-11-11-Preview
```

## Headers

```http
Content-Type : application/json
api-key : your-azure-search-key
```

## Body
```json
{
  "name":"translatingindexer", 
  "dataSourceName" : "recipes",
  "targetIndexName" : "recipeindex",
  "skillsetName" : "demoskillset",
  "fieldMappings" : [
        {
          "sourceFieldName" : "metadata_storage_path",
          "targetFieldName" : "id",
          "mappingFunction" : 
            { "name" : "base64Encode" }
        },
        {
          "sourceFieldName" : "content",
          "targetFieldName" : "content"
        }
   ],
  "outputFieldMappings" : 
  [
        {
          "sourceFieldName" : "/document/englishText", 
          "targetFieldName" : "englishText"
        }
  ],
  "parameters":
  {
    "maxFailedItems":-1,
    "maxFailedItemsPerBatch":-1,
    "configuration": 
    {
        "dataToExtract": "contentAndMetadata",
        "imageAction": "generateNormalizedImages"
        }
  }
}

```
