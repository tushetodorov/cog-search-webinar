# Creating an Index

## Type

```http
PUT
```

## URL

```http
https://your-azure-search-service-name.search.windows.net/indexes/newindex?api-version=2017-11-11-Preview
```

## Headers

```http
Content-Type : application/json
api-key : <your-azure-search-key>
```

## Body
```json
{
  "fields": [
    {
      "name": "metadata_storage_path",
      "type": "Edm.String",
      "key": true,
      "searchable": true,
      "filterable": false,
      "facetable": false,
      "sortable": true
    },
     {
      "name": "metadata_storage_name",
      "type": "Edm.String",
      "searchable": true,
      "filterable": false,
      "facetable": false,
      "sortable": true
    },
    {
      "name": "content",
      "type": "Edm.String",
      "sortable": false,
      "searchable": true,
      "filterable": false,
      "facetable": false
    },
    {
      "name": "languageCode",
      "type": "Edm.String",
      "searchable": true,
      "filterable": false,
      "facetable": false
    },
    {
      "name": "keyPhrases",
      "type": "Collection(Edm.String)",
      "searchable": true,
      "filterable": false,
      "facetable": false
    },
    {
      "name": "organizations",
      "type": "Collection(Edm.String)",
      "searchable": true,
      "sortable": false,
      "filterable": false,
      "facetable": false
    }
  ]
}
```
