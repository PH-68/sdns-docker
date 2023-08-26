# sdns-docker

1. sudo apt install nginx-module-njs

2. setup https://github.com/TuxInvader/nginx-dns

```
cd /etc/nginx/
sudo mkdir njs.d
sudo wget https://github.com/TuxInvader/nginx-dns/raw/master/njs.d/nginx_stream.js
mkdir dns && cd dns
sudo wget https://github.com/TuxInvader/nginx-dns/raw/master/njs.d/dns/dns.js
sudo wget https://github.com/TuxInvader/nginx-dns/raw/master/njs.d/dns/libdns.js
```

3. Remember to set decode and debug level to 0 in `dns.js` otherwise DNSSEC will fail

4. Copy `nginx.conf` to the bottom of `/etc/nginx/nginx.conf`

5. Copy `dns.conf` to `/etc/nginx/conf.d/dns.conf` `sudo mv dns.conf /etc/nginx/conf.d/dns.conf`
