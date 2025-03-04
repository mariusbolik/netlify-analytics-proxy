# Netlify Proxy Scripts for Analytics Services to bypass Adblockers

Netlify supports redirects and rewrites which we can use as a reverse proxy. Simply grab the matching folder for your favorite analytics service and upload it in a new Netlify project. Than start adding the domains for every project where you want to bypass adblockers.



### Posthog
```js
posthog.init('phc_ItMFP3E7rtBapLnS9FPapVjUpgJBYtHi76dULIIx7EX',
  {
    api_host: 'https://usage.example.com/ingest',
    ui_host: 'https://eu.posthog.com'
  }
)
```
https://posthog.com/docs/advanced/proxy/netlify

#### Pirsch
```html
<script defer src="https://usage.example.com/static/files/pa.js"
    id="pianjs"
    data-hit-endpoint="https://usage.example.com/p/pv"
    data-event-endpoint="https://usage.example.com/p/e"
    data-session-endpoint="https://usage.example.com/p/s"></script>
```
https://docs.pirsch.io/advanced/proxy

### Umami
```html
<script
  defer
  src="https://usage.example.com/script.js"
  data-website-id="94db1cb1-74f4-4a40-ad6c-962362670409"
  data-host-url="https://usage.example.com"
></script>
```
https://umami.is/docs/bypass-ad-blockers