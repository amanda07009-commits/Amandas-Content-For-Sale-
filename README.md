# Amanda Marsh: portfolio site

Content shoots for lifestyle businesses across Southeast Asia.

One file, `index.html`. Open it in any browser to see it; no build step, no install.

## Editing it

Everything about you is in the **CONFIG block** near the bottom of `index.html` (search for `const CONFIG`):

| What | Where in CONFIG |
|---|---|
| Name, Instagram, WhatsApp, email | `name`, `instagram`, `whatsapp`, `email` |
| Your two prices (numbers, in dollars) | `prices.halfDay`, `prices.contentDay` |
| Where you are and when you leave | `here`, `hereUntil` |
| The route | `route` (in travel order) |
| About text, portrait | `about`, `aboutIsDraft`, `portrait` |
| Testimonials | `testimonials` (the section appears when you add the first one) |
| Photos and clips | `photos` (see [photos/README.md](photos/README.md)) |
| Edited reels in the Content day | `editedReelsReady` (keep `false` until you can deliver them in 72 hours) |

While `setupMode: true`, a checklist at the top of the page shows what's still missing, and empty photo slots show as placeholders telling you which shot goes there. When the checklist is all done, set `setupMode: false` and the site is ready for clients.

## Changing the look

All colours and fonts are in the **BRAND TOKENS** block at the top of the `<style>`. Swap those values to restyle the whole site. `--grain` controls the film grain (set it to `0` to turn it off).

## Putting it on your own domain

Recommended: **Cloudflare Pages** (free, fast across Asia, works with a private repo, redeploys automatically every time this repo changes).

1. Buy the domain (e.g. `amandamarsh.com`) at Cloudflare Registrar, about $10–12 a year.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick this repo.
   Build command: none. Output directory: `/`.
3. In the new project → Custom domains → add your domain. Cloudflare sets up the DNS and HTTPS for you.
4. Update `og:image` in the `<head>` of `index.html` to the full address, e.g. `https://amandamarsh.com/photos/share.jpg`.
