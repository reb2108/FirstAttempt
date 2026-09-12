# Where the gap is in North Africa's phone app market

Research date: September 2026. Scope: Algeria, Morocco, Egypt, Tunisia.

---

## Summary

The clearest gap is **Algeria's cash-on-delivery commerce stack**. It is the largest
North African consumer market with no merchant operating system, and it stays open for a
structural reason rather than a lack of demand: the dinar is not convertible, so Stripe,
PayPal and every foreign SaaS billing model are locked out. Roughly 200,000 merchants sell
through Instagram and Facebook pages with about 1,000 of them able to take an online
payment. Everything else is cash at the door, tracked by hand.

Two credible runners-up: a diaspora bill-pay product for the Maghreb (the Aspora model,
which has no North African equivalent), and a voice-first layer for the quarter of
Moroccans who cannot read.

Several adjacent spaces look open from outside but are already contested. They are listed
at the end so they can be ruled out quickly.

---

## Gap 1: Algeria's COD commerce stack

### Demand side

| Measure | Value |
|---|---|
| Population | ~45 million |
| Internet users (end 2025) | 37.8 million, 79.5% penetration |
| Social media identities (Oct 2025) | 27.5 million, 57.7% of population |
| E-commerce market (2025) | $1.7bn to $1.9bn |
| Online merchants | ~200,000 |
| Merchants accepting online payment (June 2026) | ~1,000 |
| Orders paid cash on delivery | 85% to 95% |
| Return-to-origin rate | 15% to 20% in Algiers, Oran, Constantine |

The mismatch between 200,000 merchants and 1,000 with online payment is the whole thesis.
Selling happens in Instagram and Facebook direct messages. Payment happens at the door in
cash, or by informal bank transfer. Order tracking happens in notebooks and spreadsheets.

### Why nobody has filled it

The Algerian dinar is not freely convertible. Stripe does not operate in Algeria and
PayPal is restricted, so the gateways that work in Morocco and Egypt do not work there. A
foreign SaaS company cannot easily bill Algerian merchants or repatriate the revenue. That
single fact has kept the market clear of the platforms that crowded Morocco.

The logistics layer already exists and works. Yalidine is the largest courier, with over
160 branches covering 1,469 municipalities across all 56 provinces. ZR Express, Maystro
and NOEST handle the rest, and Ecotrack is the platform a large share of regional couriers
run on. Yalidine settles COD cash back to merchants within 24 hours, with a ceiling of
150,000 DZD per order, about $1,100. The carriers are functional but not API-first, so
integration needs middleware rather than a plug-in.

### What exists today

Only early-stage or non-commercial efforts: an open-source shipping API covering the five
main carriers, an open-source COD commerce platform, and a handful of young tools. For
contrast, Morocco has at least six competing COD platforms and confirmation-call services.
YouCan, the Moroccan store builder that did $753m in gross merchandise volume in 2023, has
only 171 live stores in Algeria.

### The sharpest wedge inside this gap

Confirmation calling in Algerian Derja. Every COD order needs a human phone call before
shipping to weed out fake orders and fix addresses, and an automated confirmation flow cuts
unconfirmed orders by 50% to 70%. Morocco already has voice agents for this, priced around
2.8 dirhams per confirmed order, working in Moroccan Darija and French. Algerian Derja is
among the least-resourced Arabic dialects for speech recognition. It appears in the
multi-dialect Casablanca dataset but has nothing like the dedicated corpora Moroccan Darija
now has. Whoever builds the Derja voice layer owns the entry point to the whole stack.

### Constraints to plan for

Billing must be collected locally in dinars, which favours a local or diaspora founder over
a foreign entrant. Merchants must satisfy CNRC registration under Law 18-05 to touch
regulated payment channels. Government policy is tailwind: the 2025 Finance Law added stamp
duty exemptions for electronic payments, the national target is 50% cashless transactions
by 2030, and a regulatory sandbox is planned for 2026 to admit at least 20 fintech startups
a year.

---

## Gap 2: Diaspora bill-pay for the Maghreb

The model is proven elsewhere and absent here. Aspora does exactly this for the Indian
diaspora: it reached a $500m valuation on a $50m Series B, onboarded 800,000 customers,
moved over $4bn, and now lets non-resident Indians pay household bills directly through
22,000 billers on India's national bill payment system, at no fee.

North Africa has the corridor volume but no equivalent product.

| Corridor fact | Value |
|---|---|
| Moroccan residents in France | over 1.5 million, the largest Moroccan diaspora anywhere |
| Morocco remittance inflows | $10.4bn, 7.9% of GDP |
| Algeria remittance inflows | $1.86bn |
| Average cost of sending from France (2019) | 6.6%, down 40% since 2013 |

France to Morocco is the single largest corridor globally for Moroccan remittances. Yet
France to Algeria and France to Tunisia remain high-cost corridors despite large migrant
populations and many providers.

The unserved need is not cheaper cash transfer, which Wise and Remitly already do 30% to
60% below Western Union. It is **control and purpose**: pay my mother's electricity bill,
top up my father's phone, settle the pharmacy account, buy the week's groceries, without
handing over cash that has to be managed at the other end. Only one small player is moving
toward this for the region.

Enter through Morocco, which has working instant payment rails and an active fintech
regulator, then extend to Algeria and Tunisia.

---

## Gap 3: A voice-first layer for people who cannot read

The capability arrived recently and no consumer product uses it.

| Measure | Value |
|---|---|
| Morocco illiteracy (2024) | 24.8%, down from 32.2% in 2014 |
| Rural Morocco | 38% |
| Moroccan women | 32.4% |
| Moroccans over 50 | 51% |
| Darija speakers | ~40 million |
| Moroccans with a mobile wallet | 6% |
| Moroccan adults unbanked | 15 million |

Atlas-Chat is the first LLM family built for Moroccan Darija, released in 2B, 9B and 27B
sizes, and the 9B beats a 13B general model on Darija benchmarks. The small sizes run in
resource-constrained settings. Darija text-to-speech and speech recognition have both
reached usable quality, with one Darija corpus of 1,000 hours reporting a 9% word error
rate.

So the models exist, and roughly one in four Moroccan adults cannot use a text interface.
Almost every app in the market is text-first, in French or Modern Standard Arabic, which is
not the language people actually speak. Nobody has shipped a voice-first consumer app for
this group. The precedents are elsewhere in Africa: Ivory Coast's voice-only Superphone
targeting the 40% who are illiterate, and Ghana's Twi-language assistant.

This is the largest gap of the three in human terms and the hardest to monetise directly.
It works best as a feature layer inside something that already earns revenue, which is why
it doubles as the wedge in Gap 1.

---

## Already contested, do not start here

- **Rotating savings circles.** Money Fellows digitised Egypt's gam'eya, processed over
  $1.5bn, passed 8 million downloads, reached profitability, and is launching in Morocco.
  Morocco's daret market is worth roughly $4bn a year, equal to 28% of bank-collected
  savings, and 88% of Moroccans using financing rely on informal services. Large, but the
  incumbent is arriving now.
- **Moroccan COD confirmation calling.** At least six services compete, several with voice
  agents already in Darija.
- **Egyptian wallets and payments.** By June 2026, 79% of Egyptian adults had a
  transactional account, 56.4 million people. The central bank is on its second financial
  inclusion strategy. Well covered.
- **Algerian ride-hailing and super-apps.** Yassir owns this and has expanded into delivery
  and financial services.
- **Moroccan agritech.** SOWIT and the state-backed Green Generation 2020-2030 programme
  hold the field, targeting 40,000 hectares by 2026.

---

## Device headwind to design around

Build for phones already in people's hands, not for next year's hardware.

| Market, Q1 2026 smartphone shipments | Change |
|---|---|
| Algeria | -28% |
| Egypt | -10% |
| Morocco | +6% |

Omdia forecasts a 28% contraction in Africa's ultra-low-cost smartphone market during 2026,
driven by memory inflation and weakening purchasing power, hitting the $80 to $150 segment
that drove adoption. Morocco grew only because import duties fell. Practical implication:
small APK size, offline-first, tolerant of poor connectivity, and low data consumption.

---

## Recommendation

Build the Algerian COD merchant stack, and lead with the Algerian Derja voice confirmation
agent as the entry product. It has verified demand, a structural barrier that keeps
better-funded foreign competitors out, per-order monetisation that a small team can
collect locally, and existing courier infrastructure to integrate rather than replace.

Gap 2 is the better fit for a founder with European regulatory access and payments
experience. Gap 3 is the better fit for a team with speech and language capability, and
should be attached to a revenue-generating product rather than sold on its own.

---

## Sources

Market and device data: Omdia via Informa, TelecomLead, DataReportal Digital 2026 Algeria,
ECDB, Statista. Financial inclusion: Central Bank of Egypt second financial inclusion
strategy 2026-2030, UNSGSA Morocco, World Bank. Algeria e-commerce and logistics: Algeria
Press Service, The North Africa Journal, DZBuild, dzecom, Ecommaps, algeriatech.news.
Remittances: IFAD, European Commission JRC, G20 National Remittance Plan France, TechCrunch
on Aspora. Language technology: Atlas-Chat (arXiv 2409.17912), Casablanca dataset (arXiv
2410.04527), MBZUAI Paris. Savings circles: Launch Base Africa on Money Fellows.
Literacy: Morocco HCP via Morocco World News, UNESCO International Literacy Day 2025.
