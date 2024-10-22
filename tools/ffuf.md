
https://github.com/ffuf/ffuf

```bash
ffuf -w /path/to/wordlist -u exploit.com/path -d "username=FUZZ" -H "Content-Type: application/x-www-form-urlencoded"


ffuf -w /path/to/wordlist:MEOW -u exploit.com/path -d "username=MEOW" -H "Content-Type: application/x-www-form-urlencoded"
```