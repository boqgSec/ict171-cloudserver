# Configuring a HTTPS with Certbot

This document will help with Installing a Cerbot, generating an SSL and changing your webpage to a HTTPS using Let's Encrypt.

# Make sure everything is up to date

```
sudo apt update
```

# Install the Cerbot

```
sudo apt install certbot python3-certbot-nginx -y
```

# Now check the status of Nginx status

```
sudo systemctl status nginx
```

output:

```
active (running
```
<img width="1055" height="286" alt="image" src="https://github.com/user-attachments/assets/911d80d9-af25-402b-9f65-9345768f391d" />

---

# Now let's install the Certbot

```
sudo certbot --nginx
```

During this process:
- You'll be asked for your email address
- Terms and conditions to accept
- The URL of the domain you're trying to certify
Your site will now be certified using Let's Encrypt

---

# Successfull SSL

You'll recieve a pop up saying Congratulatons!

<img width="844" height="41" alt="image" src="https://github.com/user-attachments/assets/c7eab004-1ae3-4bfa-baaa-f4a457e2f646" />

---

## Double check the verification

Please check your website to make sure the HTTPS is working

```
https://joshcyber.cc/
```

You'll see a successful certificate, top left of the browser.

<img width="528" height="663" alt="image" src="https://github.com/user-attachments/assets/bf1b193f-2c90-4259-856e-15cad6d25f49" />

---


## Benefits

## Used softwares
