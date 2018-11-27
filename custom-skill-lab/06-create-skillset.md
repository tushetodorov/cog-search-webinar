# Creating a Skillset

## Type

```http
PUT
```

## URL

```http
https://your-azure-search-service-name.search.windows.net/skillsets/newskillset?api-version=2017-11-11-Preview
```

## Headers

```http
Content-Type : application/json
api-key : your-azure-search-key
```

## Body
```json
{
    "description": "detect language and then translate the content",
    "skills":
    [
      {
        "@odata.type": "#Microsoft.Skills.Custom.WebApiSkill",
        "description": "Our new translator custom skill",
        "uri": "https://mytranslate.azurewebsites.net/api/Translate?code=HT9Ecx3TXb2SZaptXxAfWnTP1/fz0CJ4oM4zkFUFHLCaIZtmYDRq4w==",
        "batchSize":1,
        "context": "/document",
        "inputs": [
          {
            "name": "text",
            "source": "/document/content"
          }
        ],
        "outputs": [
          {
            "name": "text",
            "targetName": "englishText"
          }
        ]
      }
    ]
  }
  
```
