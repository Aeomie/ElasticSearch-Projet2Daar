
```
{
  "took": 4,
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
    "most_common_violations": {
      "doc_count_error_upper_bound": 0,
      "sum_other_doc_count": 122917,
      "buckets": [
        {
          "key": "10F",
          "doc_count": 30846
        },
        {
          "key": "08A",
          "doc_count": 23522
        },
        {
          "key": "06D",
          "doc_count": 14824
        },
        {
          "key": "04L",
          "doc_count": 14456
        },
        {
          "key": "02G",
          "doc_count": 13155
        }
      ]
    }
  }
}
```
