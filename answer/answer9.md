
```
{
  "took": 39,
  "timed_out": false,
  "_shards": {
    "total": 1,
    "successful": 1,
    "skipped": 0,
    "failed": 0
  },
  "hits": {
    "total": {
      "value": 3749,
      "relation": "eq"
    },
    "max_score": null,
    "hits": []
  },
  "aggregations": {
    "ViolatedCuisine": {
      "doc_count_error_upper_bound": 0,
      "sum_other_doc_count": 3208,
      "buckets": [
        {
          "key": "Chinese",
          "doc_count": 541
        }
      ]
    }
  }
}
```