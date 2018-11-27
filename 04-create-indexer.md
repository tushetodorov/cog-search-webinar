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
api-key : <your-azure-search-key>
```

## Body
```json
{
  "dataSourceName" : "newdatasource",
  "targetIndexName" : "newindex",
  "skillsetName" : "newskillset",
  "fieldMappings" : [
        {
          "sourceFieldName" : "metadata_storage_path",
          "targetFieldName" : "metadata_storage_path",
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
          "sourceFieldName" : "/document/organizations", 
          "targetFieldName" : "organizations"
        },
        {
          "sourceFieldName" : "/document/pages/*/keyPhrases/*", 
          "targetFieldName" : "keyPhrases"
        },
        {
            "sourceFieldName": "/document/languageCode",
            "targetFieldName": "languageCode"
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
