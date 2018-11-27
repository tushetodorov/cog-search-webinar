# Checking the Indexer execution status

## Type

```http
GET
```

## URLS - Multiple Queries Suggestions

```http
https://your-azure-search-service-name.search.windows.net/indexes/newindex/docs?search=cabrera&$select=keyPhrases&api-version=2017-11-11-Preview
```

```http
https://your-azure-search-service-name.search.windows.net/indexes/newindex/docs?search=linux&$select=organizations&api-version=2017-11-11-Preview
```

```http
https://your-azure-search-service-name.search.windows.net/indexes/newindex/docs?search=Microsoft&$select=keyPhrases,organizations,languageCode&api-version=2017-11-11-Preview
```


## Headers

```http
Content-Type : application/json
api-key : <your-azure-search-key>
```
