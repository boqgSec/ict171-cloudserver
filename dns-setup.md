# DNS Setup

## Purchase a Domain 

A custom domain can be bought through a domain registrar.
After a successful purchase, we can now configure the domain.


---

## DNS Management

Locate DNS records and create new A records.


| Type | Host | Value |
| --- | --- | --- |
| A    | @    | Azure IP |
| A    | www  | Azure IP |

---

# Save changes and verify

DNS saves may take a couple of seconds to hours to work, depending on the provider.

Verify the DNS is working using 

```
https://dnschecker.org
```

---

# Ping server
This command verifies that the domain is connected to the correct Azure server IP
```
ping joshcyber.cc
```


<img width="560" height="42" alt="image" src="https://github.com/user-attachments/assets/8503dd9f-1d6e-4a7b-a5e8-da8c077c77bc" />

---


## Benefits of DNS configuration
- Easier website access
- Better branding (More readable
- Protects user browsing data from being sold to third parties
- Increased security



