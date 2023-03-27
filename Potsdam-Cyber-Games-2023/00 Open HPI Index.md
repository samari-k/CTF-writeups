
# OpenHPI CTF

```toc
```




## Network

### Identity Provider

#### idp
- keycloak
-  logout: http://10.65.17.181/realms/hackhigh/protocol/openid-connect/logout

#### bookstack

- admin user exists
![](screenshots/Pasted%20image%2020230310104642.png)
- SSH user 'university-member' with password 'jumpy'

- https://github.com/BookStackApp/BookStack
- Done! You can now login using the default admin details `admin@admin.com` with a password of `password`.

bildungsurlaub
#### nextcloud
- admin user exists
- https://docs.deep-hybrid-datacloud.eu/en/latest/user/howto/rclone.html


#### legacy
![](screenshots/Pasted%20image%2020230310111240.png)



## Binary Exploitation


### key safe

![](screenshots/Pasted%20image%2020230315102438.png)


https://emn178.github.io/online-tools/sha256.html


server status flag: input 818 zeichen
passwort: timing attack

```
e73d241a8fa3cd007e2bd10ea6cc6e269259d63bedc77c8219298582532b73b4
```


get-keys:
```
<iv>
T902TQO8b1G9kkykwJTJWw==
</iv>
<ciphertext>
s/LhWjMd49tfEUWGwScwlvBQf6t5evJ+laf27NLfgnKZTjJWY6H8j30b4wdiVgkz
</ciphertext>
```


- 16 random bytes
- b64 encrypted
- 

fl4g-obfuscate
```
<iv>
3Qa/ezsDt+O2ilLOziW1Og==
</iv>
<ciphertext>
ayWKjxFGX/nUJq2LkBGnakS0UkMwPGS82Rxn7nuA1z4=
</ciphertext>
```
