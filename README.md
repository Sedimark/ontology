# SEDIMARK Marketplace Ontology

## About  
The Marketplace Information Model is an RDFS/OWL-ontology covering the fundamental concepts of SEDIMARK needed for the registration of participants and the discovery and exchange of offerings and assets. This model establishes a common framework to ensure interoperability within a SEDIMARK-based Marketplace.
This model is supported by existing proposals by similar initiatives and is built upon well-known ontologies such as Data Catalog vocabulary (DCAT), Open Digital Rights Language (ODRL), Friend Of A Friend (FOAF) or the Dublin Core Terms (DCT). In particular, the model has its foundations in the proposal shared by the International Data Spaces Protocol, to try to be compatible as much compatible as possible with such an initiative.

## Core Concepts 

### Classes
![image](/images/sedimark-ontology.png)
<!-- ![image](https://github.com/Sedimark/ontology/assets/47256078/500b801f-fb95-4b32-bed8-68506b99506f) -->

## Properties
![image](/images/sedimark-ontology-properties.png)
<!-- ![image](https://github.com/Sedimark/ontology/assets/47256078/418f9919-d235-465d-9d08-531e91d4d372) -->

## Namespaces

- SEDIMARK (Marketplace)
```
https://w3id.org/sedimark/ontology#
```
- DCAT (Data Catalogues)
```
"http://www.w3.org/ns/dcat#"
```
- DQV (Asset Quality)
```
http://www.w3.org/ns/dqv#
```
- ODRL (Asset Policies)
```
 http://www.w3.org/ns/odrl/2/
```

## Instantiation Example:
Offering provided by CVSSP living lab for ehealth monitoring.

![image](https://github.com/Sedimark/ontology/assets/47256078/c44db277-2d05-4896-9522-3b344982d8af)

### Serialisation (JSON-LD)
```json
{
  "@graph": [
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/living-lab-01",
      "@type": [
        "owl:NamedIndividual",
        "dct:Location"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/health-monitoring-morning-period",
      "@type": [
        "owl:NamedIndividual",
        "dct:PeriodOfTime"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/ehealth-living-lab",
      "dct:title": {
        "@value": "E-health Living Lab",
        "@type": "rdfs:Literal"
      },
      "dct:hasPart": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/surrey-local-catalogue"
      },
      "dct:publisher": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP"
      },
      "dct:language": {
        "@value": "English",
        "@type": "rdfs:Literal"
      },
      "@type": [
        "Self-Listing",
        "owl:NamedIndividual"
      ],
      "dct:rights": "This work is licensed under Creative Commons Attribution-NoDerivatives 4.0 International.\nhttps://creativecommons.org/licenses/by-nd/4.0/",
      "dct:issued": {
        "@value": "2024-01-01",
        "@type": "rdfs:Literal"
      },
      "belongsTo": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP"
      },
      "hasOffering": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001"
      },
      "dct:description": {
        "@value": "Self-listing for the ehealth-living-lab data provision",
        "@type": "rdfs:Literal"
      },
      "dct:modified": {
        "@value": "2024-01-02",
        "@type": "rdfs:Literal"
      },
      "dct:creator": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP"
      }
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/surrey-local-catalogue",
      "@type": [
        "owl:NamedIndividual",
        "dcat:Catalog"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP",
      "https://purl.org/dc/terms/description": {
        "@language": "en",
        "@value": ""
      },
      "http://xmlns.com/foaf/0.1/name": {
        "@language": "en",
        "@value": ""
      },
      "hasSelf-Listing": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/ehealth-living-lab"
      },
      "http://xmlns.com/foaf/0.1/openid": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-open-id-profile"
      },
      "http://xmlns.com/foaf/0.1/homepage": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-homepage"
      },
      "http://xmlns.com/foaf/0.1/account": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-online-account"
      },
      "dct:description": {
        "@value": "",
        "@type": "rdfs:Literal"
      },
      "@type": [
        "owl:NamedIndividual",
        "Participant"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001",
      "hasOfferingContract": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/wearable-contract"
      },
      "dct:issued": {
        "@value": "2024-01-02",
        "@type": "rdfs:Literal"
      },
      "dct:language": {
        "@value": "English",
        "@type": "rdfs:Literal"
      },
      "hasAsset": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001"
      },
      "dct:title": {
        "@value": "Wearable data for Subject 001",
        "@type": "rdfs:Literal"
      },
      "dct:temporal": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/health-monitoring-morning-period"
      },
      "@type": [
        "owl:NamedIndividual",
        "Offering"
      ],
      "dcat:temporalResolution": {
        "@value": "P6H",
        "@type": "xsd:duration"
      },
      "dct:publisher": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP"
      },
      "dct:description": {
        "@value": "This offering provides data assets with data originating from wearable sensors on smart watches",
        "@type": "rdfs:Literal"
      },
      "dcat:dataset": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001"
      },
      "dct:creator": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP"
      },
      "dct:created": {
        "@value": "2024-01-01",
        "@type": "rdfs:Literal"
      },
      "dct:isPartOf": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/ehealth-living-lab"
      },
      "http://xmlns.com/foaf/0.1/homepage": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-homepage"
      }
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-open-id-profile",
      "@type": [
        "owl:NamedIndividual",
        "http://xmlns.com/foaf/0.1/Document"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001",
      "hasAssetQuality": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001-quality"
      },
      "http://purl.org/dc/elements/1.1/identifier": {
        "@value": "cvssp-livinglab-wearable-steps-001",
        "@type": "rdfs:Literal"
      },
      "http://purl.org/dc/elements/1.1/creator": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/CVSSP"
      },
      "http://purl.org/dc/elements/1.1/title": {
        "@value": "Steps Dataset for Subject 001",
        "@type": "rdfs:Literal"
      },
      "http://purl.org/dc/elements/1.1/description": {
        "@value": "This dataset captures data from step counter on wearable smart watch for subject 001",
        "@type": "rdfs:Literal"
      },
      "@type": [
        "owl:NamedIndividual",
        "https://w3id.org/sedimark/vocab#DataAsset"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001-quality",
      "@type": [
        "owl:NamedIndividual",
        "AssetQuality"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/agreement-001",
      "references": {
        "@id": "https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001"
      },
      "@type": [
        "owl:NamedIndividual",
        "Agreement"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/wearable-contract",
      "@type": [
        "owl:NamedIndividual",
        "OfferingContract"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-homepage",
      "@type": [
        "owl:NamedIndividual",
        "http://xmlns.com/foaf/0.1/Document"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/wearable-001-license-doc",
      "dct:rights": {
        "@value": "This work is licensed under Creative Commons Attribution-NoDerivatives 4.0 International.\nhttps://creativecommons.org/licenses/by-nd/4.0/",
        "@type": "rdfs:Literal"
      },
      "dct:license": {
        "@value": "This work is licensed under Creative Commons Attribution-NoDerivatives 4.0 International.\nhttps://creativecommons.org/licenses/by-nd/4.0/",
        "@type": "rdfs:Literal"
      },
      "@type": [
        "owl:NamedIndividual",
        "dct:LicenseDocument"
      ]
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-online-account",
      "http://xmlns.com/foaf/0.1/accountName": {
        "@language": "en",
        "@value": ""
      },
      "@type": [
        "owl:NamedIndividual",
        "http://xmlns.com/foaf/0.1/OnlineAccount"
      ]
    },
    {
      "@id": "https://creativecommons.org/licenses/by/4.0/",
      "rdfs:label": {
        "@value": "ontology license",
        "@type": "rdfs:Literal"
      },
      "@type": "owl:NamedIndividual"
    },
    {
      "@id": "https://sedimark.surrey.ac.uk/ecosystem/cvssp-contact-email",
      "@type": "owl:NamedIndividual"
    },
    {
      "@id": "https://sedimark.eu/wp-content/uploads/2023/11/sedimark_logo_512x512.png",
      "@type": "owl:NamedIndividual"
    }
  ],
  "@context": {
    "sedi": "https://w3id.org/sedimark/ontology#",
    "dct": "http://purl.org/dc/terms/",
    "owl": "http://www.w3.org/2002/07/owl#",
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "xml": "http://www.w3.org/XML/1998/namespace",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "dcat": "http://www.w3.org/ns/dcat#",
    "@vocab": "https://w3id.org/sedimark/ontology#"
  }
}
```
## SPARQL Query Example (1):

```sparql
prefix sedi: <https://w3id.org/sedimark/ontology#>
prefix owl: <http://www.w3.org/2002/07/owl#>
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
prefix xml: <http://www.w3.org/XML/1998/namespace>
prefix xsd: <http://www.w3.org/2001/XMLSchema#>
prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>
prefix dcat: <http://www.w3.org/ns/dcat#>
prefix dct: <http://purl.org/dc/terms/>


SELECT * WHERE {
  ?participant a sedi:Participant .
  ?participant sedi:hasSelf-Listing ?selflisting .
  ?selflisting dct:hasPart ?localCat.
  ?selflisting sedi:hasOffering ?offering .
  ?offering sedi:hasAsset ?asset .
  ?asset sedi:hasAssetQuality ?assetquality .
  ?offering dcat:temporalResolution ?tempRes .  
  
} LIMIT 10

```

- Result (CSV):

```csv
participant,selflisting,localCat,offering,asset,assetquality,tempRes
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,https://sedimark.surrey.ac.uk/ecosystem/ehealth-living-lab,https://sedimark.surrey.ac.uk/ecosystem/surrey-local-catalogue,https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001-quality,P6H
```
## SPARQL Query Example (2): Participant information
```sparql
prefix sedi: <https://w3id.org/sedimark/ontology#>
prefix owl: <http://www.w3.org/2002/07/owl#>
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
prefix xml: <http://www.w3.org/XML/1998/namespace>
prefix xsd: <http://www.w3.org/2001/XMLSchema#>
prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>
prefix dcat: <http://www.w3.org/ns/dcat#>
prefix dct: <http://purl.org/dc/terms/>

SELECT * WHERE {
   ?participant a sedi:Participant .   
   ?participant ?p ?o .
}
```
- Result (CSV):

```csv
participant,p,o
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://www.w3.org/1999/02/22-rdf-syntax-ns#type,https://w3id.org/sedimark/ontology#Participant
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://www.w3.org/1999/02/22-rdf-syntax-ns#type,http://www.w3.org/2002/07/owl#NamedIndividual
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://purl.org/dc/terms/description,""
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://xmlns.com/foaf/0.1/account,https://sedimark.surrey.ac.uk/ecosystem/cvssp-online-account
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://xmlns.com/foaf/0.1/homepage,https://sedimark.surrey.ac.uk/ecosystem/cvssp-homepage
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://xmlns.com/foaf/0.1/openid,https://sedimark.surrey.ac.uk/ecosystem/cvssp-open-id-profile
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,https://w3id.org/sedimark/ontology#hasSelf-Listing,https://sedimark.surrey.ac.uk/ecosystem/ehealth-living-lab
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,http://xmlns.com/foaf/0.1/name,""
https://sedimark.surrey.ac.uk/ecosystem/CVSSP,https://purl.org/dc/terms/description,""

```

## SPARQL Query Example (3): Offering information
```sparql
prefix sedi: <https://w3id.org/sedimark/ontology#>
prefix owl: <http://www.w3.org/2002/07/owl#>
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
prefix xml: <http://www.w3.org/XML/1998/namespace>
prefix xsd: <http://www.w3.org/2001/XMLSchema#>
prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>
prefix dcat: <http://www.w3.org/ns/dcat#>
prefix dct: <http://purl.org/dc/terms/>

SELECT * WHERE {
   ?offering a sedi:Offering .   
   ?offering ?p ?o .
}
```

- Result (CSV):

```csv
offering,p,o
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://www.w3.org/1999/02/22-rdf-syntax-ns#type,https://w3id.org/sedimark/ontology#Offering
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://www.w3.org/1999/02/22-rdf-syntax-ns#type,http://www.w3.org/2002/07/owl#NamedIndividual
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/issued,2024-01-02
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/description,This offering provides data assets with data originating from wearable sensors on smart watches
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/created,2024-01-01
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/creator,https://sedimark.surrey.ac.uk/ecosystem/CVSSP
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/isPartOf,https://sedimark.surrey.ac.uk/ecosystem/ehealth-living-lab
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/language,English
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/publisher,https://sedimark.surrey.ac.uk/ecosystem/CVSSP
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/temporal,https://sedimark.surrey.ac.uk/ecosystem/health-monitoring-morning-period
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://purl.org/dc/terms/title,Wearable data for Subject 001
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://www.w3.org/ns/dcat#dataset,https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://xmlns.com/foaf/0.1/homepage,https://sedimark.surrey.ac.uk/ecosystem/cvssp-homepage
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,https://w3id.org/sedimark/ontology#hasAsset,https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,https://w3id.org/sedimark/ontology#hasOfferingContract,https://sedimark.surrey.ac.uk/ecosystem/wearable-contract
https://sedimark.surrey.ac.uk/ecosystem/wearable-offering-001,http://www.w3.org/ns/dcat#temporalResolution,P6H
```

## SPARQL Query Example (4): Asset information

```sparql
prefix sedi: <https://w3id.org/sedimark/ontology#>
prefix owl: <http://www.w3.org/2002/07/owl#>
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
prefix xml: <http://www.w3.org/XML/1998/namespace>
prefix xsd: <http://www.w3.org/2001/XMLSchema#>
prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>
prefix dcat: <http://www.w3.org/ns/dcat#>
prefix dct: <http://purl.org/dc/terms/>

SELECT * WHERE {
   ?dataAsset a sedi:DataAsset .   
   ?dataAsset ?p ?o .
}
```

- Result (CSV):

```csv
dataAsset,p,o
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,http://www.w3.org/1999/02/22-rdf-syntax-ns#type,https://w3id.org/sedimark/vocab#DataAsset
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,http://www.w3.org/1999/02/22-rdf-syntax-ns#type,http://www.w3.org/2002/07/owl#NamedIndividual
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,http://purl.org/dc/elements/1.1/description,This dataset captures data from step counter on wearable smart watch for subject 001
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,http://purl.org/dc/elements/1.1/title,Steps Dataset for Subject 001
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,http://purl.org/dc/elements/1.1/creator,https://sedimark.surrey.ac.uk/ecosystem/CVSSP
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,http://purl.org/dc/elements/1.1/identifier,cvssp-livinglab-wearable-steps-001
https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001,https://w3id.org/sedimark/ontology#hasAssetQuality,https://sedimark.surrey.ac.uk/ecosystem/steps-asset-001-quality
```  

## Licence
This is licensed under a Creative Commons Attribution 4.0 International License.

## Acknowledgement
This work is funded by the European Union under the Horizon Europe framework programme [grant no. 101070074]. 
This project is also partly funded by UK Research and Innovation (UKRI) under the UK government’s Horizon Europe funding guarantee [grant no. 10043699].
