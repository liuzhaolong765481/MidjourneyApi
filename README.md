# midjourneyApi

#### 支持
- Midjourney api Generate Image
- Midjourney upsample、variation、etc

- Mj api Generate Image
- Mj upsample、variation、etc


### Usage method
- first, if you don't have [ Rapid ](https://rapidapi.com) account, please register、activation and login, 
- then go to [ Midjourney API](https://rapidapi.com/liuzhaolong765481/api/midjourney-best-experience) and subscribe to the basic free program and then you can use it to your work
- If you have any questions, please contact me via email by 1552519081@qq.com

### PHP Demo
```
<?php

$curl = curl_init();

curl_setopt_array($curl, [
	CURLOPT_URL => "https://midjourney-best-experience.p.rapidapi.com/mj/generate-fast?prompt=a beautiful cat --ar 1920:1080&hook_url=https://www.google.com",
	CURLOPT_RETURNTRANSFER => true,
	CURLOPT_ENCODING => "",
	CURLOPT_MAXREDIRS => 10,
	CURLOPT_TIMEOUT => 30,
	CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
	CURLOPT_CUSTOMREQUEST => "POST",
	CURLOPT_HTTPHEADER => [
		"X-RapidAPI-Host: midjourney-best-experience.p.rapidapi.com",
		"X-RapidAPI-Key: your api key"
	],
]);

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
	echo "cURL Error #:" . $err;
} else {
	echo $response;
}
```

### Python Demo

```
import requests

url = "https://midjourney-best-experience.p.rapidapi.com/mj/generate-fast"

querystring = {"prompt":"a beautiful cat --ar 1920:1080","hook_url":"https://www.google.com/"}

headers = {
	"X-RapidAPI-Key": "your api key",
	"X-RapidAPI-Host": "midjourney-best-experience.p.rapidapi.com"
}

response = requests.post(url, headers=headers, params=querystring)

print(response.json())
```
