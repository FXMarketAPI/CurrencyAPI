
# FXMarketAPI
FXMarketAPI is easy to use JSON REST API with both live and historical currency exchange rates for over 40 currencies. Data is sourced from an aggregated feed of institutional providers (not a broker feed) giving you reliable and up-to date traded rates that are used by banks globally. We have systems in place to remove irregular prices, giving you the cleanest prices available. Our API powers applications and financial software in major financial insitutions all around the world.

# Overview
## Authentication with API Key
API key can be accessed by signing up to the service. The API's data endpoints can be accessed using the api_key. To access the data, add your api_key to the URL endpoint: following is an example of an API call to access live data:

### Request Example:
```url
https://fxmarketapi.com/apilive?currency=EURUSD,GBPUSD,USDJPY&api_key=api_key
```

## JSON Response
Our API will respond with a JSON object. For more details see below.

### Response Example:
```json
  {
    "timestamp": 1541012848,
    "price": {
      "EURUSD": 1.1323,
      "GBPUSD": 1.2776,
      "USDJPY": 112.9855
    }
  }
```

The API will return timestamp and price object containing requested currency pairs exchange rates and timestamp

### Response Parameters:
Field	Type	Description
timestamp	integer	UNIX time of the price in seconds
price	JSON object	Contains all currency pair codes (string) and their respective exchange rates (float).
Available Currencies
A list of all the available currencies can be accessed through requesting the API or clicking the link stated here. To access JSON object containing all available currency codes and names, simply append your api_key to the fxmarketapi apicurrencies endpoint:

### Request Example:
```url
https://fxmarketapi.com/apicurrencies?api_key=api_key
```
### Response Example:
```json
{
    "currencies": {
      "USDAED": "United Arab Emirates Dirham",
      "USDARS": "Argentine Peso",
      "AUDUSD": "Australian Dollar",
      "USDBRL": "Brazilian Real",
      "BTCUSD": "Bitcoin",
      "USDCAD": "Canadian Dollar",
      "USDCHF": "Swiss Franc",
      "USDCLP": "Chilean Peso",
      "USDCNY": "Chinese Yuan",
      "USDCOP": "Colombian Peso",
      "EURCZK": "Czech Republic Koruna",
      "EURDKK": "Danish Krone",
      "EURUSD": "Euro",
      "GBPUSD": "British Pound Sterling",
       "[...]"
   }
}
```

### Response Parameters:
Field	Type	Description
currencies	JSON Object	Returns all currency pair codes and thier names in a (string) format that are available through the API
Endpoints
The FXMarketAPI API has five endpoints serving different sets of data. Below is a summary of these endpoints.


### Available Endpoints:
URL Endpoints
```url
https://fxmarketapi.com/apilive?&api_key

https://fxmarketapi.com/apihistorical?date=YYYY-MM-DD&api_key

https://fxmarketapi.com/apitimeseries?start_date=2015-01-01&end_date=2015-05-01&api_key

https://fxmarketapi.com/apichange?currency=EURUSD,EURGBP&api_key
```

## HTTPS Encryption
Paid and non-paid members both can access secure connection(SSL).      
