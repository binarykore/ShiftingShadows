# Docker Shadow Socks:

* export SSPASSWORD=SET_PASSWORD_HERE
* docker run -d -p 7331:7331 oddrationale/docker-shadowsocks -s 0.0.0.0 -p 7331 -k $SSPASSWORD -m aes-256-cfb
* sslocal -c ~/ss.json -d start

# Save in Format as SS.json

```{
  "server":"0.0.0.0",
  "server_port":7331,
  "local_address": "127.0.0.1",
  "local_port":1080,
  "password":"$SSPASSWORD",
  "timeout":600,
  "method":"aes-256-cfb"
}```
