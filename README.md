

### Requetes

- Q1: List all the neighborhoods in New York.
```
GET ny_restau_final/_search
{
  "size": 0,
  "aggs": {
    "neighborhoods": {
      "terms": {
        "field": "NTA",
        "size": 5000
      }
    }
  }
}
```
- Q2: Which neighborhood has the most restaurants?
```
GET ny_restau_final/_search
{
  "size": 0,
  "aggs": {
    "most_populated_neighborhood": {
      "terms": {
        "field": "NTA",
        "size": 1,
        "order": {
          "_count": "desc"
        }
      }
    }
  }
}
```
- Q3: What does the violation code "04N" correspond to?
```
GET ny_restau_final/_search
{
  "size": 1,
  "_source": ["VIOLATION DESCRIPTION"],
  "query": {
    "term": {
      "VIOLATION CODE": "04N"
    }
  }
}

```

- Q4: Where are the restaurants (name, address, neighborhood) that have a grade of A?
```
GET ny_restau_final/_search
{
  "size":10000,
  "_source": ["DBA","STREET","NTA"],
  "query": {
    "term": {
      "GRADE": "A"
    }
  }
}
```
- Q5: What is the most popular cuisine? And by neighborhood?
```
GET ny_restau_final/_search
{
  "size": 0,
  "aggs": {
    "most_popular_cuisine": {
      "terms": {
        "field": "CUISINE DESCRIPTION",
        "size": 1,
        "order": {
          "_count": "desc"
        }
      }
    },
    "by_neighborhood": {
      "terms": {
        "field": "NTA",
        "size": 100,
        "order": {
          "_count": "desc"
        }
      },
      "aggs": {
        "top_cuisine": {
          "terms": {
            "field": "CUISINE DESCRIPTION",
            "size": 1,
            "order": {
              "_count": "desc"
            }
          }
        }
      }
    }
  }
}
```
- Q6: What is the date of the last inspection?
```
GET ny_restau_final/_search
{
  "size": 0,
  "aggs": {
    "last_inspection": {
      "max": {
        "field": "INSPECTION DATE"
      }
    }
  }
}
```
- Q7: Provide a list of Chinese restaurants with an A grade in Brooklyn.

```
GET ny_restau_final/_search
{
  "size":10000,
  "_source": ["DBA"],
  "query": {
    "bool": {
      "must": [
        {
          "match": {
            "CUISINE DESCRIPTION": "Chinese"
          }
        },
        {
          "term": {
            "GRADE": "A"
          }
        },
        {
          "term": {
            "BORO": "Brooklyn"
          }
        }
      ]
    }
  }
}
```
- Q8: What is the address of the restaurant LADUREE?

```
GET ny_restau_final/_search
{ 
  "_source": ["STREET", "BORO", "BUILDING", "ZIPCODE"],
  "query": {
    "match": {
      "DBA": "LADUREE"
    }
  }
}
```

- Q9: What cuisine is most affected by the violation "Hot food item not held at or above 140º F"?

```
GET ny_restau_final/_search
{
  "size": 0,
  "query": {
    "match_phrase": {
      "VIOLATION DESCRIPTION": "Hot food item not held at or above 140º F"
    }
  },
  "aggs": {
    "ViolatedCuisine": {
      "terms": {
        "field": "CUISINE DESCRIPTION",
        "size": 1,
        "order": {
          "_count": "desc"
        }
      }
    }
  }
}
```

- Q10: What are the most common violations (Top 5)?
```
GET ny_restau_final/_search
{
  "size":0,
  "aggs": {
    "most_common_violations": {
      "terms": {
        "field": "VIOLATION CODE",
        "size": 5,
        "order": {
          "_count": "desc"
        }
      }
    }
  }
}
```
- Q11: What is the most popular restaurant chain?
```

GET ny_restau_final/_search
{
  "size":0,
  "aggs": {
    "Mostpopular_Restau": {
      "terms": {
        "field": "CAMIS",
        "size": 1,
        "order": {
          "_count": "desc"
        }
      }
    }
  }
}

# Q11 with name
GET ny_restau_final/_search
{
  "size": 0,
  "aggs": {
    "Mostpopular_Restau": {
      "terms": {
        "field": "CAMIS",
        "size": 1,
        "order": {
          "_count": "desc"
        }
      },
      "aggs": {
        "restaurant_name": {
          "top_hits": {
            "_source": ["DBA"],
            "size": 1
          }
        }
      }
    }
  }
}
```