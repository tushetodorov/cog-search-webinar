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
api-key : your-azure-search-key
```

## Body
```json
{
  "fields": [
    {
      "name": "id",
      "type": "Edm.String",
      "key": true,
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
      "name": "englishText",
      "type": "Edm.String",
      "sortable": false,
      "searchable": true,
      "filterable": false,
      "facetable": false
    }
  ]
}
```
