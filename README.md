# measurement-spec
DRAFT strawman proposal for a pecification for how to communicate measurement information

Strawman:

```jsonc
{
  "imp": {
    "ext": {
      "dooh": { // can we land grab "dooh" as an extension namespace?
        "venuetypeid": 1234,
        "measurement": {
          "imp_x": 12.3433
          "provider": "measurement.co", // can also be the publisher if self-rated
          "data_sources": ["highway-data.org","ticket-vendor.com"],
          "adjustments": [3],
        }
    }
  }    
}
```

## Key Concepts:

`imp_x` - estimated number of individuals potentially exposed to an ad, should a bidder win this auction

`provider` - reference a registry with info like name, website or reverse TLD similarly to how we might identify pubishers?

`data_sources` additional datasources (also identified by domain? if incorporated into measurement estimate

`adjustments` - list of ways numbers may have been adjusted
  1. Evenly spread over time period
  2. Spread over time period based on typical dwell time
  3. Spread over time period based on third-party traffic pattern estimates
  4. Spread over time period based on publisher traffic pattern estimates
  5. Adjusted based on hours-of-operation
