# ornginxcok2ed

#### HTTP/2 Server Push
```
location = /demo.html {
  http2_push /style.css
  http2_push /image1.jpg
}
```
- Server must be configured for http/2
- NGINX can also automatically push resources to clients if proxied applications include an HTTP reponse
header named Link

## 9. Sophiscated Media Streaming
```
server {
  location /video/ {
    mp4;
  }
  location ~\.flv$ {
    flv;
  }
}
```
