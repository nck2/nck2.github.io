

  <div class="input_area" markdown="1">
  
```python
import os
import sys
import urllib.request
```

  </div>
  

  <div class="input_area" markdown="1">
  
```python
client_id = "QTKf81BA4QcR0mz_e5tc"
client_secret = "Wbvq8_eYhh"
encText = urllib.parse.quote("학교에 가고 싶다.")
data = "source=ko&target=en&text=" + encText
url = "https://openapi.naver.com/v1/language/translate"
request = urllib.request.Request(url)
request.add_header("X-Naver-Client-Id",client_id)
request.add_header("X-Naver-Client-Secret",client_secret)
response = urllib.request.urlopen(request, data=data.encode("utf-8"))
rescode = response.getcode()
if(rescode==200):
    response_body = response.read()
    print(response_body.decode('utf-8'))
else:
    print("Error Code:" + rescode)
```

  </div>
  
  {:.output_stream}
  ```
  {"message":{"@type":"response","@service":"naverservice.labs.api","@version":"1.0.0","result":{"translatedText":"I want to go to school."}}}

  ```
  

  <div class="input_area" markdown="1">
  
```python
type(response_body)
```

  </div>
  



  {:.output_data_text}
  ```
  bytes
  ```
  



  <div class="input_area" markdown="1">
  
```python
import json
```

  </div>
  

  <div class="input_area" markdown="1">
  
```python
result2=json.loads(response_body)
```

  </div>
  

  <div class="input_area" markdown="1">
  
```python
result2
```

  </div>
  



  {:.output_data_text}
  ```
  {'message': {'@service': 'naverservice.labs.api',
  '@type': 'response',
  '@version': '1.0.0',
  'result': {'translatedText': 'I want to go to school.'}}}
  ```
  



  <div class="input_area" markdown="1">
  
```python
type(result2)
```

  </div>
  



  {:.output_data_text}
  ```
  dict
  ```
  



  <div class="input_area" markdown="1">
  
```python
print(result2['message'])
```

  </div>
  
  {:.output_stream}
  ```
  {'@type': 'response', '@service': 'naverservice.labs.api', '@version': '1.0.0', 'result': {'translatedText': 'I want to go to school.'}}

  ```
  

  <div class="input_area" markdown="1">
  
```python
print(result2['message']['result']['translatedText'])
```

  </div>
  
  {:.output_stream}
  ```
  I want to go to school.

  ```
  

  <div class="input_area" markdown="1">
  
```python

```

  </div>
  