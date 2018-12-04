
# JavaScript (jQuery.ajax)
## Below is an example for live exchange rates data using jQuery:

var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://fxmarketapi.com/apilive?currency=USDJPY,AUDUSD,GBPUSD,EURUSD&api_key=api_key",
  "method": "GET",
  "headers": {}
  }

$.ajax(settings).done(function (response) {
  console.log(response);
});
