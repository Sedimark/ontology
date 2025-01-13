## Context
The [context](https://sedimark.github.io/ontology/broker/jsonld-contexts/sedimark-compound.jsonld) define all
the already discussed property for types :
- [Asset](https://sedimark.github.io/ontology/broker/jsonld-contexts/sedimark-asset.jsonld)
- [DataAsset](https://sedimark.github.io/ontology/broker/jsonld-contexts/sedimark-data-asset.jsonld)
- [AIModelAsset](https://sedimark.github.io/ontology/broker/jsonld-contexts/sedimark-ai-model-asset.jsonld)
- [ServiceAsset](https://sedimark.github.io/ontology/broker/jsonld-contexts/sedimark-service-asset.jsonld)

## Calling the broker with the context
You can use the "Link" header to define the context of your request when calling the NGSILD-Broker.
```
<https://sedimark.github.io/ontology/broker/jsonld-contexts/sedimark-compound.jsonld>; rel="http://www.w3.org/ns/json-ld#context"; type="application/ld+json"
```

An example of asset creation for a broker deployed on "localhost:8080" would be the following :

POST "localhost:8080/ngsi-ld/v1/entities"

body :
```json
{
  "id": "urn:ngsi-ld:Asset:MyAssetId",
  "type": "Asset",
  "title": {
    "type": "Property",
    "value": "my Title"
  },
  "creator": {
    "type": "Relationship",
    "value": "id:of:the:creator"
  },
  "description": {
    "type": "Property",
    "value": "my Description"
  },
  "publisher": {
    "type": "Relationship",
    "value": "id:of:the:publisher"
  },
  "issued": {
    "type": "Property",
    "value": "2024-09-01T11:00:00.000Z"
  },
  "modified": {
    "type": "Property",
    "value": "2024-09-01T11:00:00.000Z"
  },
  "keyword": {
    "type": "Property",
    "value": ["Tag1", "Tag2"]
  },
  "license": {
    "type": "Property",
    "value": "https://creativecommons.org/licenses/by-nd/4.0/"
  },
  "spatial": {
    "type": "Property",
    "value": "myValue"
  },
  "wasGeneratedBy": {
    "type": "Property",
    "value": "myValue"
  },
  "used": {
    "type": "Property",
    "value": "myValue"
  },
  "startedAtTime": {
    "type": "Property",
    "value": "2024-01-01T01:00:00.000Z"
  },
  "endedAtTime": {
    "type": "Property",
    "value": "2024-12-31T23:59:59.000Z"
  },
  "version": {
    "type": "Property",
    "value": "v1.1"
  },
  "endpointURL": {
    "type": "Property",
    "value": "https://my.endpoint/url"
  },
  "endpointDescription": {
    "type": "GeoProperty",
    "value": "this is what my endpoint do"
  },
  "geometry": {
    "type": "Property",
    "value": "myValue"
  },
  "image": {
    "type": "Property",
    "value": "https://image.com/my/image"
  },
  "relatedAsset": {
    "type": "Property",
    "value": "myValue"
  },
  "processingSteps": {
    "type": "Property",
    "value": "myValue"
  },
  "location": {
    "type": "GeoProperty",
    "value": { // any geoJson
      "type": "Point",
      "coordinates": [
        1.5,
        1.5
      ]
    }
  },

}

```