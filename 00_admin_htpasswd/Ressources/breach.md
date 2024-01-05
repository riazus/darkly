# 00_admin_htpasswd

### Instructions

Inside the [host]/robots.txt file, there is a /whatever path. Navigating to this path allows us to discover the following:
`root:437394baff5aa33daa618be47b75cb49`
After decrypting using the MD5 algorithm, the password becomes qwerty123@.
Attempting to sign in with these credentials on the path /admin grants access to the admin page.

### How to prevent

1. Protect the htpasswd file.
2. Conceal robots.txt from public access.
