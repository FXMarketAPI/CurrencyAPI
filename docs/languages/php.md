

# PHP (CURL)
## Below is an example for live exchange rates data using PHP (CURL):

?php

$curl = curl_init();

curl_setopt_array( $curl, array(
  CURLOPT_PORT => "5000",
  CURLOPT_URL => "https://fxmarketapi.com/apilive?currency=USDJPY,AUDUSD,GBPUSD,EURUSD&api_key=api_key",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
