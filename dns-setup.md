# DNS Setup

## Purchase a Domain 

A custom domain can be bought through a domain registrar.
After a successful purchase, we can now configure the domain.


---

## DNS Management

Locate DNS records and create new A records.


| Type | Host | Value |
| --- | --- | --- |
| A    | @    | 52.184.82.227 |
| A    | www  | 52.184.82.227 |

<img width="1001" height="193" alt="image" src="https://github.com/user-attachments/assets/695de59e-7fda-49d6-bbd3-e50fd4c44845" />

---

# Save changes and verify

DNS propagation may take anywhere from a couple of seconds to hours, depending on the provider.

Verify the DNS is working using 

```
https://dnschecker.org
```

---

# Verify Domain
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



