# Web

## Scripting requests

It is common in web-challenges that you need to script your requests. Python is good for that.

You can make a request really easy, like this. If you don't have `requests` installed you can install it with `pip install requests`.

**Basic request**

```
import requests

req = requests.get("http://site.com")
print req.status_code
print req.text
```

**Request with custom header**

```
import requests

headers = {
"Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8",
"Accept-Encoding": "gzip, deflate, sdch",
"Accept-Language": "en-US,en;q=0.8,es;q=0.6,sv;q=0.4",
"Cache-Control": "max-age=0",
"Connection": "keep-alive",
"Referer": "https://www.google.com/",
"User-Agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.82 Safari/537.36"
}

req = requests.get("http://site.com", headers=headers)
print req.status_code
print req.text
```

**Add an get action**

```
values = {'action' : 'whatever'}
req = requests.get("http://site.com", data=values, headers=headers)
```



