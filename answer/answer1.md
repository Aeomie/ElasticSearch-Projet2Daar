```
{
  "took": 5,
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
    "neighborhoods": {
      "doc_count_error_upper_bound": 0,
      "sum_other_doc_count": 161838,
      "buckets": [
        {
          "key": "MN17",
          "doc_count": 12195
        },
        {
          "key": "MN13",
          "doc_count": 6442
        },
        {
          "key": "MN23",
          "doc_count": 6312
        },
        {
          "key": "MN24",
          "doc_count": 6281
        },
        {
          "key": "MN27",
          "doc_count": 5113
        },
        {
          "key": "MN22",
          "doc_count": 4996
        },
        {
          "key": "QN22",
          "doc_count": 4598
        },
        {
          "key": "MN15",
          "doc_count": 4210
        },
        {
          "key": "MN25",
          "doc_count": 4124
        },
        {
          "key": "MN19",
          "doc_count": 3878
        }
      ]
    }
  }
}
```