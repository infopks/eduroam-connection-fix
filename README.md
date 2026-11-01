# eduroam-connection-fix

Fixes and troubleshooting tools for eduroam connections.

## Linux kernel 7.0+ login issue

Just in case anyone is having the same issue, here is an update for the eduroam login issue on Linux kernel 7.0+:

**1st command:**

```bash
sudo nmcli connection modify eduroam 802-1x.eap ttls 802-1x.phase2-auth pap 802-1x.identity "your_university_email" 802-1x.anonymous-identity "anonymous@uniroma1.it" 802-1x.password "your_password" 802-1x.password-flags 0 802-1x.phase1-auth-flags 32
```

**2nd command:**

```bash
sudo nmcli --ask connection up eduroam
```

Replace the example identity, anonymous identity, and password with your institution's values. Do not commit real credentials to a repository or share them publicly. If your password includes a trailing period, make sure it remains inside the password quotes.

Thank you!
