# 07_header_spoof

## Instruction

In the page

```
http://192.168.56.101/index.php?page=b7e44c7a40c5f80139f0a50f3650fb2bd8d00b0d24667c4c2ca32c88e13b758f
```

We'll get several hints several hints such as `You must come from : "https://www.nsa.gov/"` and `Let's use this browser : "ft_bornToSec". It will help you a lot.`

Using provided information we can write next curl request

```
curl 'http://192.168.56.101/?page=b7e44c7a40c5f80139f0a50f3650fb2bd8d00b0d24667c4c2ca32c88e13b758f' -H "Referer: https://www.nsa.gov/" -H "User-Agent: ft_bornToSec" -s -o head.html
```

After request let's find our flag

```
cat head.html | grep flag
```

## How to prevent

The finally responsibility for security always rests with the back-end.
We should always check every request that came from the internet
