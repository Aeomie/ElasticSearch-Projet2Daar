
```
{
  "took": 0,
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
    "most_populated_neighborhood": {
      "doc_count_error_upper_bound": 0,
      "sum_other_doc_count": 207792,
      "buckets": [
        {
          "key": "MN17",
          "doc_count": 12195
        }
      ]
    }
  }
}

```