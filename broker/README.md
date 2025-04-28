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

body : [example here](https://sedimark.github.io/ontology/broker/payload-example/asset.jsonld)
