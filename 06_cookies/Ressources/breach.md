# 06_cookies

## Instruction

Website contains `I_am_admin` cookie. If we decrypt his value with MD5, we'll get `false`.
Let encrypt `true` and paste him as a value.

```
b326b5062b2f0e69046810717534cb09
```

## How to prevent

Store sensitive data in the memory of front-end (e.g. redux)
Or use cookies which have decryption key in the back-end.
