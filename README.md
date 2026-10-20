# alloochauffeur.com

Static one-page site for Allo Chauffeur, a VTC driver in Toulouse. No build step.

## Deploy (Cloudflare Pages)

1. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → `netsalary/alloochauffeur.com`
2. Framework preset: **None**. Build command: *(empty)*. Output directory: `/`
3. After the first deploy: Custom domains → add `alloochauffeur.com` and `www.alloochauffeur.com`

Every push to `main` redeploys automatically.

## Placeholders to replace

| What | Where |
|---|---|
| Phone (WhatsApp + call) | `PHONE_INTL` and `PHONE_DISPLAY` at the top of the script in `index.html`, plus `telephone` in the JSON-LD block |
| Fixed prices / routes | `routes` array in `index.html` |
| VTC registry n° and SIRET | footer of `index.html` and `mentions-legales.html` |
| Owner name, address, insurance, VTC card n° | `mentions-legales.html` |

## How booking works

The form builds a pre-filled WhatsApp message and opens `wa.me/<number>`. The customer taps Send, and the request lands in the driver's WhatsApp. No backend needed.

## Legal note

Never use the word "taxi" on the site or in ads. Only licensed taxis may use it. Use "VTC", "chauffeur privé" or "transfert aéroport".
