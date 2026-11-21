# cleanX — Chicago cleaning quotes

Live site: https://cleanx.haxcomputer.com/

## Credit and acknowledgment

cleanX is a revamped fork of [howyoungx/illini-move-clean](https://github.com/howyoungx/illini-move-clean). The original website, visual design, animations, chat interface, pricing-panel experience, images, icons, and backend implementation are credited to **howyoungx and the original Illini Move & Clean contributors**. The original 20-commit history and authorship remain preserved.

- Original website: https://howyoungx.github.io/illini-move-clean/
- Imported revision: e52a40c7dcf1c673698730d6d7b3c006a3566011

The cleanX owner has confirmed permission from the original author for experimental reuse. This does not imply endorsement or grant additional rights to third parties.

## cleanX adaptation

The original visual shell, responsive pricing panel, service tiles, gradients and chat-card design are retained. cleanX uses Chicago coverage and its own residential rates and monthly commercial contract ranges. The cleanX map is a separate copy of the supplied north/south coverage polygons, with cleanX branding and no Maye's Cleaning reference.

Residential bases: under 1,000 sq ft $50 Standard / $80 move-in/out; 1,000–2,000 $100 / $130; 2,001–3,000 $150 / $180. Bedroom and bathroom tier totals are added separately. Deep bundle adds $70 for fridge, stove and cabinets, without double charging. Homes above 3,000 sq ft require a custom quote. See calculate() in index.html and _worker.js for the complete approved rules; keep both copies synchronized.

Commercial: month-to-month monthly USD/sq-ft ranges: office .09–.15, retail .07–.15, medical .14–.25, industrial .08–.20, education .07–.13. Visit frequency is scope information and never multiplies the monthly estimate.

## Hosting and connections

Cloudflare Pages project cleanx-illini deploys main with no build command and output directory '.'. The root _worker.js uses env.ASSETS for the static site. Add a Workers AI binding named AI. The assistant uses @cf/openai/gpt-oss-20b; no AI API key is exposed in the browser. AI inputs are capped and rate limited per server instance; the calculator remains available if AI is unavailable. Free quotas apply. These in-memory limits are a basic guard, not a durable global quota.

/api/chat returns a conversational response plus a server-calculated price card. /api/quote-prepare validates contact fields and recomputes the price before returning an email payload. After the customer explicitly confirms the request, the browser posts that payload using FormSubmit AJAX to dani@hax.support, without opening an email application. FormSubmit requires recipient activation. Requests are estimates only; no payment or confirmed booking is created. Final scope, coverage, availability and price are confirmed by cleanX.

The browser keeps the current chat in memory only. Contact details are sent to Cloudflare for validation and to FormSubmit for email delivery after consent. Do not collect payment, medical or other sensitive data in chat or forms.

The imported worker/ directory is retained for source history and reference, is not deployed as the cleanX backend, and is blocked from static serving. Original company AI, inbox and payment endpoints are not used by the deployed cleanX page. No Stripe or deposit collection is enabled.

The previous haxsupport/cleanX repository and cleanx-39w.pages.dev deployment remain available as a fallback. Only cleanx.haxcomputer.com was reassigned; the main HaxComputer website is separate.
