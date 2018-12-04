# Python
## Below is an example for live exchange rates data using Python:

import requests

url = "https://fxmarketapi.com/apilive"

querystring = {"currency":"USDJPY","api_key":"api_key"}

response = requests.get(url, params=querystring)

print(response.json())
