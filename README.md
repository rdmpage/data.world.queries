# data.world.queries
Example queries for data on data.world. For some documentation see https://meta.data.world/apis-at-data-world-cfa1e308bdc8#.5voil0thj

## SPARQL endpoint

The SPARQL endpoint is https://query.data.world/sparql/<data> where <data> is the name of the data set. For example, for https://data.world/zika-virus-data/mosquito-data the data set is  **zika-virus-data/mosquito-data**, so the SPARQL endpoint is https://query.data.world/sparql/zika-virus-data/mosquito-data

To query the endpoint you need to authorise the query using your API key, which you get from your settings page https://data.world/settings/advanced . Put this value in the “Authorisation” header.


## Zika virus geography

```
SELECT ?id ?lat ?lon
WHERE {
  ?row <http://data.world/zika-virus-data/mosquito-data/aegypti_albopictus.csv/aegypti_albopictus#OCCURRENCE_ID> ?id .
  ?row <http://data.world/zika-virus-data/mosquito-data/aegypti_albopictus.csv/aegypti_albopictus#X_raw>  ?lat .
  ?row <http://data.world/zika-virus-data/mosquito-data/aegypti_albopictus.csv/aegypti_albopictus#Y_raw>  ?lon .

}
LIMIT 10

```

Response from SPARQL:
```
{
    "query_text": "SELECT ?id ?lat ?lon\nWHERE {\n  ?row <http://data.world/zika-virus-data/mosquito-data/aegypti_albopictus.csv/aegypti_albopictus#OCCURRENCE_ID> ?id .\n  ?row <http://data.world/zika-virus-data/mosquito-data/aegypti_albopictus.csv/aegypti_albopictus#X_raw>  ?lat .\n  ?row <http://data.world/zika-virus-data/mosquito-data/aegypti_albopictus.csv/aegypti_albopictus#Y_raw>  ?lon .\n\n}\nLIMIT 10",
    "query_lang": "SPARQL",
    "head": {
        "vars": [
            "id",
            "lat",
            "lon"
        ]
    },
    "results": {
        "bindings": [
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "1"
                },
                "lat": {
                    "type": "literal",
                    "value": "40.07"
                },
                "lon": {
                    "type": "literal",
                    "value": "-3.22"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "2"
                },
                "lat": {
                    "type": "literal",
                    "value": "15.3"
                },
                "lon": {
                    "type": "literal",
                    "value": "-4.27"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "11"
                },
                "lat": {
                    "type": "literal",
                    "value": "-80.99"
                },
                "lon": {
                    "type": "literal",
                    "value": "25.49"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "101"
                },
                "lat": {
                    "type": "literal",
                    "value": "-81.78"
                },
                "lon": {
                    "type": "literal",
                    "value": "24.55"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "1001"
                },
                "lat": {
                    "type": "literal",
                    "value": "-47.8"
                },
                "lon": {
                    "type": "literal",
                    "value": "-21.16"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "10001"
                },
                "lat": {
                    "type": "literal",
                    "value": "7.37"
                },
                "lon": {
                    "type": "literal",
                    "value": "6.55"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "10002"
                },
                "lat": {
                    "type": "literal",
                    "value": "7.37"
                },
                "lon": {
                    "type": "literal",
                    "value": "6.55"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "10003"
                },
                "lat": {
                    "type": "literal",
                    "value": "-1.62"
                },
                "lon": {
                    "type": "literal",
                    "value": "6.69"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "10004"
                },
                "lat": {
                    "type": "literal",
                    "value": "-1.58"
                },
                "lon": {
                    "type": "literal",
                    "value": "6.72"
                }
            },
            {
                "id": {
                    "type": "literal",
                    "datatype": "http://www.w3.org/2001/XMLSchema#integer",
                    "value": "10005"
                },
                "lat": {
                    "type": "literal",
                    "value": "-1.47"
                },
                "lon": {
                    "type": "literal",
                    "value": "6.72"
                }
            }
        ]
    }
}
```