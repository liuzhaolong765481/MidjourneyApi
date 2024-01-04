# midjourneyApi

#### 支持
- Midjourney Api Generate Image
- Midjourney upsample(U1 U2...)、variation(V1 V2...)、etc
- Midjourney Api Describe Image
- Midjourney Api Dlend Image


### Usage method
- first, register [ ttapi ](https://ttapi.io/register) account, 
- then go to [ TTApi Center](https://ttapi.io/center) to get TT-API-KEY, and you can use the midjouney api doc:https://doc.mjapiapp.com/
- If you have any questions, please contact me  in telegram https://t.me/voyagell

### PHP Demo
```
<?php

$url = 'https://api.ttapi.io/midjourney/v1/imagine';

$data = array(
    'prompt' => 'a cat --ar 1:1',
    'model' => 'fast',
    'hookUrl' => ''
);

$ch = curl_init($url);

$dataString = json_encode($data);

curl_setopt($ch, CURLOPT_CUSTOMREQUEST, "POST");
curl_setopt($ch, CURLOPT_POSTFIELDS, $dataString);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_HTTPHEADER, array(
    'Content-Type: application/json',
    'TT-API-KEY: your_key'
);

$result = curl_exec($ch);

$httpCode = curl_getinfo($ch, CURLINFO_HTTP_CODE);

curl_close($ch);

echo $httpCode;


```

### Python Demo

```
import requests

endpoint = "https://api.ttapi.io/midjourney/v1/imagine"

headers = {
    "TT-API-KEY": your_key
}

data = {
    "prompt": "a cute cat",
    "model": "fast",
    "hookUrl": ""
}

response = requests.post(endpoint, headers=headers, json=data)

print(response.status_code)
print(response.json())

```
