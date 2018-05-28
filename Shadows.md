# How to setup Shadowsocks on your Ubuntu server

Your school or company network may block the access to a few specific websites. To solve this problem, I'd highly recommend Shadowsocks, since it is the easiest proxy tool I've ever found, and it's FREE (of course iff you have your own server running).

First, `ssh` to your server, and make sure you have Python and `pip` installed. If you have Python but not `pip`, install it using the following command

```bash
$ sudo apt-get install python3-pip
```

Then, install Shadowsocks using `pip`

```bash
$ sudo pip install shadowsocks
```

Create configuration file at `/etc/shadowsocks.json`, with the following content,

```json
{
   "server":"[server ip address]",
   "server_port":8388,
   "local_port":0,
   "password":"[password]",
   "timeout":600,
   "method":"aes-256-cfb"
}
```

Don't forget to change the `[server ip address]` and `[password]` in the block above.

Finally, we're ready to start the shadowsocks server that runs in the background by 

```bash
$ sudo ssserver -c /etc/shadowsocks.json -d start
```

If you wish to stop the Shadowsocks server, do this

```bash
$ sudo ssserver -c /etc/shadowsocks.json -d stop
```

To install Shadowsocks client software on your local machine, follow the instruction in [this repository on GitHub](https://github.com/shadowsocks/shadowsocks-gui).

Cheers! Now you don't ever need to curse your school or company Internet administrator for blocking your favorite websites anymore.
