# Verum

Proyecto nuevo e interesante de rastreo. Pronto más detalles.

## DNS Setup

### En tu proveedor de dominio (qd.je), agrega:

**GitHub Pages (A records):**
```
A  verum.qd.je  185.199.108.153
A  verum.qd.je  185.199.109.153
A  verum.qd.je  185.199.110.153
A  verum.qd.je  185.199.111.153
```

**Zoho Mail (MX records):**
```
MX 10  zmxhost01.zoho.com
MX 20  zmxhost02.zoho.com
```

**Zoho Domain Verification (CNAME):**
```
CNAME  zbXXXXXXX  zmverify.zoho.com
```

**Zoho SPF (TXT record):**
```
TXT  v=spf1 include:zoho.com ~all
```

## Deploy

```bash
git init
git add .
git commit -m "init"
gh repo create verum-email --public --push
# En GitHub: Settings > Pages > Custom domain: verum.qd.je
```
