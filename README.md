# The George Org

Public company site for **thegeorgeorg.org** — parent of mash.baby, Mutiny, and d-Tech.

Small static pages so the business has a live website (needed for toll-free SMS signup). No app server.

## Local

```bash
python3 -m http.server 8766 --directory site
# http://127.0.0.1:8766/
```

## Fly

```bash
fly deploy --ha=false
```

App: `thegeorgeorg` (region `ord`). Live at https://thegeorgeorg.org and https://www.thegeorgeorg.org.

| Type | Name | Value |
|------|------|--------|
| A | `@` | `66.241.124.24` |
| AAAA | `@` | `2a09:8280:1::185:36b8:0` |
| CNAME | `www` | `thegeorgeorg.fly.dev` |
| CNAME | `_acme-challenge` | `thegeorgeorg.org.rk8dkd3.flydns.net` |
| CNAME | `_acme-challenge.www` | `www.thegeorgeorg.org.rk8dkd3.flydns.net` |

Outlook email DNS (MX / SPF / autodiscover / Microsoft 365 CNAMEs) stays on GoDaddy and must not be removed when changing A / AAAA / www.
