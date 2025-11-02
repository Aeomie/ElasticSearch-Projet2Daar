

```

{
  "took": 64,
  "timed_out": false,
  "_shards": {
    "total": 1,
    "successful": 1,
    "skipped": 0,
    "failed": 0
  },
  "hits": {
    "total": {
      "value": 10000,
      "relation": "gte"
    },
    "max_score": null,
    "hits": []
  },
  "aggregations": {
    "by_neighborhood": {
      "doc_count_error_upper_bound": 0,
      "sum_other_doc_count": 161838,
      "buckets": [
        {
          "key": "MN17",
          "doc_count": 12195,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 8297,
            "buckets": [
              {
                "key": "American",
                "doc_count": 3718
              }
            ]
          }
        },
        {
          "key": "MN13",
          "doc_count": 6442,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 4679,
            "buckets": [
              {
                "key": "American",
                "doc_count": 1656
              }
            ]
          }
        },
        {
          "key": "MN23",
          "doc_count": 6312,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 4759,
            "buckets": [
              {
                "key": "American",
                "doc_count": 1474
              }
            ]
          }
        },
        {
          "key": "MN24",
          "doc_count": 6281,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 5075,
            "buckets": [
              {
                "key": "American",
                "doc_count": 1155
              }
            ]
          }
        },
        {
          "key": "MN27",
          "doc_count": 5113,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 3642,
            "buckets": [
              {
                "key": "Chinese",
                "doc_count": 1416
              }
            ]
          }
        },
        {
          "key": "MN22",
          "doc_count": 4996,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 4118,
            "buckets": [
              {
                "key": "American",
                "doc_count": 816
              }
            ]
          }
        },
        {
          "key": "QN22",
          "doc_count": 4598,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 1924,
            "buckets": [
              {
                "key": "Chinese",
                "doc_count": 2603
              }
            ]
          }
        },
        {
          "key": "MN15",
          "doc_count": 4210,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 3228,
            "buckets": [
              {
                "key": "American",
                "doc_count": 935
              }
            ]
          }
        },
        {
          "key": "MN25",
          "doc_count": 4124,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 2863,
            "buckets": [
              {
                "key": "American",
                "doc_count": 1219
              }
            ]
          }
        },
        {
          "key": "MN19",
          "doc_count": 3878,
          "top_cuisine": {
            "doc_count_error_upper_bound": 0,
            "sum_other_doc_count": 2948,
            "buckets": [
              {
                "key": "American",
                "doc_count": 902
              }
            ]
          }
        }
      ]
    },
    "most_popular_cuisine": {
      "doc_count_error_upper_bound": 0,
      "sum_other_doc_count": 184410,
      "buckets": [
        {
          "key": "American",
          "doc_count": 36449
        }
      ]
    }
  }
}
```