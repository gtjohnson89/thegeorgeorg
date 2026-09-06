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

App: `thegeorgeorg` (region `ord`). Custom domain certs: `thegeorgeorg.org` and `www.thegeorgeorg.org`.

Outlook email DNS (MX / SPF / autodiscover) stays on GoDaddy and must not be removed when changing A / AAAA / www.
