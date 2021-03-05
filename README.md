# measurement-spec
DRAFT strawman proposal for a pecification for how to communicate measurement information

Strawman:

```json
{
  "imp": {
    "ext": {
      "dooh": {
        "venuetypeid": 1234,
        "measurement": {
          "provider_id": 1,
          "data_sources": [],
          "adjustments": [3],
          "imp_x": 12.3433
        }
    }
  }    
}
```

Key Concepts:

* Provider - reference a registry with info like name, corporate id? (D&B? something else?), website
* Adjustments - list of ways numbers may have been adjusted
** 1 = Evenly spread over time period
** 2 = Spread over time period based on typical dwell time
** 3 = Spread over time period based on third-party traffic pattern estimates
** 4 = Spread over time period based on publisher traffic pattern estimates
