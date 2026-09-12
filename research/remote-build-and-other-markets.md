# Other markets, native demand, and whether this can be built remotely

Part three. Companion to `north-africa-app-market-gap.md` and
`algeria-cod-product-and-projections.md`. Research date: September 2026.

---

## Summary

**The remote constraint inverts the earlier recommendation.** Algeria was attractive
precisely because the dinar is not convertible, which locks out Stripe and every
foreign competitor. That same fact means an Algerian merchant has no legal way to
pay a foreign company. Local CIB and Edahabia cards are not approved for
international payments. Algerian merchants already buy Meta ads through local
reseller agencies that invoice in dinars, because they cannot pay Meta directly.

So Algeria is the single worst market in this set for a remote founder, for exactly
the reason it looked best.

**Natives have expressed the need, clearly and in their own words.** Two Algerian
open-source projects exist specifically to solve this, with explicit problem
statements. That is the strongest demand signal available, and simultaneously the
strongest competitive warning: they are building it themselves, for free, and one
of them names per-transaction pricing as part of the problem.

**Three business shapes survive the remote test.** Sell to the diaspora side in
euros, sell to the couriers instead of the merchants, or pick a market with working
card rails. Morocco and the Philippines pass. Algeria does not.

---

## Part 1: Native demand, in their own words

This is primary evidence from people in the market, not analyst reports.

### CodFlow, an open-source COD platform for Algeria

Built by an Algerian developer. Its stated motivation:

> "E-commerce in Algeria is 95%+ Cash on Delivery. Western platforms like Shopify
> and local tools charge per-transaction fees, require expensive VPS hosting, and
> lock your data in their databases."

The problems it lists: transaction fees of 2 to 5 percent per order plus software
fees eating margins, vendor lock-in, fragmented carrier integration across
Yalidine, ZR Express, NOEST and Ecotrack, inadequate driver management, and ad
spend optimised against orders rather than against deliveries that actually
succeed. It claims doorstep refusal rates of 30 to 50 percent.

It describes itself as "the first and only open-source COD e-commerce platform
built for Algeria," with zero transaction fees and full data ownership.

### dzship, a unified courier API

Built by DZBuild, which says it processes real COD orders across Algeria daily. It
covers 99 Algerian couriers behind one interface. Its problem statement:

> "Every Algerian courier ships its own API: different auth, different field names,
> statuses in French, Arabic, or bare numbers, and documentation that ranges from
> thin to wrong."

It also names silent failure modes: misspelled communes, undocumented validation
steps, inverted status codes, and integrations that pass a demo but strand parcels
in production. Its philosophy: "These guides exist so you don't relearn each trap
the expensive way."

### What this evidence actually tells you

Four things, and two of them are bad news.

1. **The pain is real and specific.** Nobody writes a 99-courier abstraction layer
   for fun. The fragmentation I described in part one is worse than I said: 99
   couriers, not five.
2. **The confirmation and delivery-success problem is independently confirmed** by
   an operator, including the observation that ad optimisation is misaligned with
   delivery success. That is a product insight I had not identified.
3. **Local builders resent the pricing model I proposed.** CodFlow names
   per-transaction fees as a grievance and offers zero-fee as its main selling
   point. A foreign entrant charging per confirmed order is walking into an
   articulated objection, with a free alternative already published.
4. **The refusal-rate claim of 30 to 50 percent is an outlier.** Other Algerian
   sources put normal return-to-origin at 8 to 15 percent, typical practice around
   20 percent, and anything past 30 percent as loss-making. The 20 percent falling
   to 13 percent used in part two remains the defensible assumption.

### Limits of this evidence

I could not reach Reddit, the Shopify app store reviews, the Shopify community
forums, or Twitter within this session. The native voices above are developers and
platform operators, not a sample of ordinary merchants. Before committing capital,
talk to actual sellers. The developer evidence establishes that the problem is
real; it does not establish willingness to pay.

---

## Part 2: Other markets

Every one of these is a bigger COD market than Algeria, or an easier one, or both.

| Market | COD share of orders | Return-to-origin | Market size | Can a merchant pay a foreign company? |
|---|---|---|---|---|
| **Pakistan** | 95%+ | 30–45% reported; 18–20% national average | $5.2 bn (2023) | Hard. State Bank restricts foreign exchange dealings |
| **Egypt** | 51% to over 70% | — | $9–11 bn | Partly. Paddle supports Egypt |
| **Philippines** | 68% of buyers | 20–40% | — | Yes, cards and wallets work |
| **Indonesia** | ~38% to over 70% | 15–20% | large | Generally yes |
| **Morocco** | 70%+ | 18–25% | — | **Yes, explicitly legal** |
| **Nigeria** | 70%+ | — | — | Partly |
| **Iraq** | COD-dominant | — | — | Partly. Paddle supports Iraq |
| **Algeria** | 85–95% | 15–25% | $1.9 bn | **No** |

### Pakistan is the biggest prize

95 percent of transactions are cash on delivery, more than 30 percent of the
population has no bank account, and reported return-to-origin runs 30 to 45 percent
against Algeria's 15 to 25. The market was $5.2 bn in 2023, roughly three times
Algeria's.

It also has the best documented proof that the product works. Brands that
implement WhatsApp confirmation within five minutes of an order see return rates
fall from 30–35 percent to 18–22 percent inside the first month. Requiring a 10
percent deposit cuts return rates by 30 to 45 percent.

The catch is the same shape as Algeria's, milder. Pakistan's State Bank restricts
foreign exchange dealings to authorised entities, Shopify Payments and Stripe do
not operate there, and recurring billing in rupees through a local provider is
rare. Pakistani founders routinely solve this with a US or UK entity, but that
works for billing foreign customers, not for collecting from local ones.

### Morocco is the best remote fit in North Africa

Morocco's exchange regulations for 2026 create an explicit annual e-commerce
allowance covering exactly this use case: 20,000 dirhams for an individual, up to 2
million for a startup carrying the digital agency label, and up to 5 million for a
company. The allowance specifically covers subscribing to foreign software
services. The overall annual foreign payment ceiling is 500,000 dirhams per person.

So a Moroccan merchant can legally and practically pay a foreign subscription. At
roughly $37 a month, a single merchant consumes about a fifth of the individual
allowance a year. That is headroom, not a constraint.

The cost is competition. Morocco already has at least six confirmation and COD
operations platforms, several running voice agents in Darija. It is the opposite
trade from Algeria: easy to bill, hard to win.

### One competitor already spans seven of these markets

A platform called eGrow markets COD operations tooling across Morocco, the United
Arab Emirates, India, Egypt, Pakistan, Nigeria and the Philippines, combining a
WhatsApp agent handling text, voice and images in more than 50 languages with
regional carrier integrations and order management. It claims 78 percent autonomous
resolution. I could not reach its site directly to verify, so treat the
capabilities as claimed rather than confirmed.

The generic version also exists on the Shopify app store, where several COD
confirmation and verification apps are published with real review counts. The
multi-country play is contested. The dialect-specific, carrier-specific play is
where the defensibility lives.

---

## Part 3: Can this be built completely remotely?

Not as originally specified. The Algeria plan requires collecting money in dinars
from merchants who cannot pay foreign companies, which requires a local entity or a
reseller partner. That is not a remote business.

Three shapes do work remotely. They are ordered by how well they fit the constraint.

### Shape A: Sell to the diaspora, bill in euros

This is the strongest remote fit, and it is the second gap from part one rather
than the first.

The sender lives in France, Spain, Italy, Belgium or the Netherlands. You bill them
in euros with ordinary European card rails. The Maghreb side is a payout
destination, not a billing problem, so the dinar never touches your revenue. France
alone hosts more than 1.5 million Moroccan residents, Morocco receives $10.4 bn a
year at 7.9 percent of GDP, and the France-to-Algeria and France-to-Tunisia
corridors remain expensive despite large migrant populations.

The obstacle is regulatory, not technical. Money remittance is a licensed activity.
The realistic route in is to register as an **agent of an existing authorised
payment institution** rather than seek your own licence. Agent registration takes
roughly 4 to 12 weeks with a well-prepared due diligence file, and the sponsoring
institution carries the capital requirement, which for remittance-only permissions
starts at €20,000. EU jurisdictions follow a comparable framework under the second
Payment Services Directive.

That is a genuinely remote-compatible business: European customers, European
billing, a licensing path that does not require you to be anywhere in particular.

### Shape B: Sell to the couriers, not the merchants

Instead of billing 36,000 Algerian merchants who cannot pay you, bill the handful
of carriers who can. Yalidine, Ecotrack and the larger couriers are real companies
with corporate banking and a direct financial interest in fewer failed deliveries,
because they eat the cost of the wasted trip.

One contract replaces a consumer-scale collections problem. It is also the
defensive move against the biggest competitive risk identified in part two, which
was a courier building this itself.

The trade is obvious: a handful of buyers with all the leverage, and a much smaller
revenue ceiling than owning the merchant relationship.

### Shape C: Pick a market with working card rails

If you want the merchant-facing product, build it where merchants can pay. On the
evidence above that means **Morocco** or the **Philippines** first, then Indonesia
and Egypt. The Philippines adds two advantages for a remote founder: business is
conducted in English, and 68 percent of buyers pay cash on delivery with return
rates of 20 to 40 percent, so the problem is as acute as Algeria's.

Morocco is easier to bill and harder to win. The Philippines is further away
culturally and linguistically from anything the earlier research covered, but the
commercial mechanics are the friendliest of the set.

### What does not work remotely

Algeria as a merchant-billing market. Not because of the product, the demand or the
competition, but because the payment rail does not exist and the workaround, a
local reseller invoicing in dinars, is a local business with staff and an entity.
If you want Algeria, the realistic structure is a local co-founder who owns the
entity and the collections while you own the product. That is a different plan from
the one in part two, and it is not remote.

---

## Revised recommendation

If the constraint is genuinely remote-only, build **Shape A**: diaspora bill-pay
for the Maghreb, billing European senders in euros, entering as the registered
agent of an authorised payment institution. It is the only one of the three that is
both large and structurally suited to being run from anywhere.

Keep the Algerian COD stack on the shelf. The demand evidence for it is the
strongest of anything found across all three parts, and two Algerian teams are
already validating it in public. It becomes buildable the moment you have a local
partner, and not before.

If you want to stay merchant-facing and remote, **Morocco or the Philippines** are
the markets to test, in that order for North Africa and reversed if you weight
English-language operations and card availability above cultural proximity.

---

## Sources

Native project evidence: CodFlow and dzship repository documentation on GitHub.
Payment rails: Morocco Office des Changes IGOC 2026 via Upsilon Consulting,
Pakistan State Bank foreign exchange framework via Oxford Business Law Blog,
Stripe and Paddle country availability listings, Algerian payment workarounds via
dzecom and Grey. Market data: ECDB, DHL Pakistan, eGrow, Cloud Ecommerce
Philippines, Selligate, eHub. Licensing: UK Financial Conduct Authority payment
institution guidance, RemitONE, PSP Lab.
