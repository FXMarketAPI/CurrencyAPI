
#API Features
for full list of features visit http://fxmarketapi/documentation#live_rates

## Live Rates
The FXMarketAPI API's live endpoint's provides a Real-Time exchange rates feed to the users.

### Request Example:
```
https://fxmarketapi.com/apilive
?api_key=kIqpioVq-PUc_oTQAsJp
& currency=EURUSD,GBPUSD,USDJPY,AUDUSD
```
### Respose:

```
{
  "timestamp": 1541521247,
  "price": {
    "AUDUSD": 0.7225,
    "EURUSD": 1.1412,
    "GBPUSD": 1.3079,
    "USDJPY": 113.3845
  }
}
```
### Request Example:
```
https://fxmarketapi.com/apihistorical
?api_key=kIqpioVq-PUc_oTQAsJp
&date=2018-05-02
```
### Response:
```
{
  "date": "2018-05-02",
  "price": {
    "EURUSD": 1.19509,
    "GBPUSD": 1.35748,
    "USDJPY": 109.8405
  }
}
```
### Request Example:
```
  https://fxmarketapi.com/apitimeseries
  ?api_key=kIqpioVq-PUc_oTQAsJp
  & currency=EURUSD,GBPUSD
  & start_date=2018-07-02
  & end_date=2018-09-02
```
Response:
```
{
  "start_date": "2018-07-02",
  "end_date": "2018-09-02",
  "price": {
      "2018-07-02": {
        "EURUSD": {
          "close": 1.1639,
          "high": 1.1692,
          "low": 1.1591,
          "open": 1.168
        },
        "GBPUSD": {
          "close": 1.3143,
          "high": 1.3212,
          "low": 1.3095,
          "open": 1.3194
        }
      },
      "2018-07-03": {
        "EURUSD": {
          "close": 1.1658,
          "high": 1.1673,
          "low": 1.162,
          "open": 1.1639
        },
        "GBPUSD": {
          "close": 1.3192,
          "high": 1.3208,
          "low": 1.3115,
          "open": 1.315
        }
      },
      "..."
   }
}
```
### Request Example:
```
https://fxmarketapi.com/apichange
?api_key=kIqpioVq-PUc_oTQAsJp
& currency=EURUSD,GBPUSD
& start_date=2018-07-02
& end_date=2018-09-02
```
### Response:
```
{
  "start_date": "2018-07-02",
  "end_date": "2018-09-02",
  "price": {
    "EURUSD": {
      "change": 0.0038,
      "end_rate": 1.1601,
      "pct_change": -0.3299,
      "start_rate": 1.16394
    },
    "GBPUSD": {
      "change": 0.0183,
      "end_rate": 1.296,
      "pct_change": -1.3909,
      "start_rate": 1.31428
  }
}
}
```
