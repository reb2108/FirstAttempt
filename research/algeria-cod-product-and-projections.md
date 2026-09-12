# Algeria COD stack: product examples and projected usage

Companion to `north-africa-app-market-gap.md`. Research date: September 2026.
Exchange rate throughout: 130 DZD to the dollar (2026 average was 129.79).

---

## Part 1: What the product actually is

Four components, shipped in this order. The first one alone is a business; the
other three are what stops a courier from copying it.

### 1. The confirmation agent (the wedge)

Every cash-on-delivery order in Algeria needs a phone call before it ships. The
call filters orders that were never serious, catches a wrong address before the
courier wastes a trip, and restates the total so the customer is not surprised at
the door. Merchants do this by hand, often for hours a day. Morocco has automated
it in Darija; Algeria has not.

An illustrative call flow in Algerian Derja. Transliteration needs validation by
native speakers before any of this ships.

| Step | Derja | English |
|---|---|---|
| Open | *Salam 3alikoum, hadi mokalama men [Boutique].* | Hello, this is a call from [shop]. |
| Identify order | *3andna commande b'ismek: [product].* | We have an order in your name: [product]. |
| Confirm price | *[price] dinar, plus [fee] dinar livraison. Total [total] dinar. Sah?* | [price] dinars plus [fee] delivery. Total [total]. Correct? |
| Confirm address | *L'adresse: [commune], wilaya [wilaya]. Sahih?* | The address is [commune], [wilaya] province. Right? |
| Confirm availability | *Rak tkoun mawjoud nhar [day]?* | Will you be there on [day]? |
| Close | *Chokran, commande confirmée. Yji 3andek [day].* | Thank you, order confirmed. It arrives [day]. |

Three behaviours matter more than the script:

- **Escalate, don't loop.** Anything the agent cannot resolve in two turns goes to a
  human queue with a transcript attached. A bad automated call costs more than no call.
- **Code-switching is the default, not an edge case.** Algerian speech moves between
  Derja, French and Modern Standard Arabic inside a single sentence, and product
  names are usually French or English. The agent has to handle that mid-utterance.
- **Filter, don't just confirm.** Repeat orders from one number to different names,
  addresses that fail geocoding, and totals the customer disputes are all signals.
  Score them and let the merchant decide before shipping.

### 2. The order board

One screen replacing the notebook: every order with its state (awaiting
confirmation, confirmed, dispatched, out for delivery, refused, returned, cash
settled). Cash reconciliation is the part nobody else does. Couriers reimburse
daily, and merchants currently match those deposits to orders by hand.

### 3. The courier router

Five carriers with different coverage, price and reliability by province.
Delivery runs 400 to 900 DZD depending on carrier, destination and weight, and
northern provinces are cheaper than southern. Yalidine is the only carrier that
reliably reaches the south, at 160 branches across 1,469 municipalities. The
router picks per parcel on cost, coverage and that carrier's recent refusal rate
in that province, then books through one integration instead of five.

### 4. The upsell moment

The confirmation call is a live conversation with a buyer who has already decided.
That is the highest-intent moment in the whole funnel and it is currently dead
air. Offer one accessory or a quantity bump during the call, and charge commission
only on accepted offers. Morocco prices this at roughly $0.50 per accepted offer.

---

## Part 2: Three worked merchant examples

Assumes the confirmation flow cuts return-to-origin by 7 to 10 points, consistent
with reported reductions of 50 to 70 percent in unconfirmed orders. Failed
delivery costed conservatively at 700 DZD, return fee only.

### Amine, phone accessories, Bab Ezzouar

80 orders a month, 5,500 DZD basket, 35% gross margin, return rate 22% falling to 13%.

| | Before | After |
|---|---|---|
| Orders delivered | 62 | 70 |
| Revenue | 343,200 DZD | 382,800 DZD |
| Failed-delivery cost | 12,320 DZD | 7,280 DZD |
| Tool cost | 0 | 4,900 DZD |
| **Net** | **107,800 DZD** | **121,800 DZD** |

Gains 14,000 DZD a month, about $108, on $38 of spend. Return of 3.9x, plus the
hours a day he stops spending on the phone.

### Lila, modest fashion, Oran

320 orders a month, 7,200 DZD basket, 42% margin, return rate 25% falling to 15%.

| | Before | After |
|---|---|---|
| Orders delivered | 240 | 272 |
| Revenue | 1,728,000 DZD | 1,958,400 DZD |
| Failed-delivery cost | 56,000 DZD | 33,600 DZD |
| Tool cost | 0 | 12,100 DZD |
| **Net** | **669,760 DZD** | **776,828 DZD** |

Gains 107,068 DZD a month, about $824, on $93 of spend. Return of 9.8x. She is
the ideal customer and she is also the one who already employs someone to make
these calls.

### The hobbyist, Setif

18 orders a month, 4,800 DZD basket, 30% margin. **Roughly break-even, and
negative on a thin basket.** The fixed platform fee eats the entire gain.

Break-even sits around 13 to 20 orders a month depending on basket size and
margin. Below that the per-order fee is still profitable for the merchant but the
monthly platform fee is not. **Pricing implication:** per-order only at the bottom
of the market, with the platform fee switching on above a volume threshold. This
is also why the addressable merchant base is far smaller than the headline
200,000.

---

## Part 3: Deriving order volume

No published figure exists for Algerian parcel volume, so it has to be built and
shown rather than cited.

| Step | Value | Source or assumption |
|---|---|---|
| E-commerce revenue 2025 | $1,716 M | ECDB |
| Growth applied for 2026 | 12.5% | ECDB projects 10 to 15% |
| E-commerce revenue 2026 | $1,930 M | derived |
| Physical goods share | 70% | assumption, strips travel and digital |
| Physical goods GMV | $1,351 M | derived |
| Cash-on-delivery share | 90% | reported range 85 to 95% |
| **COD GMV 2026** | **$1,216 M** | derived |
| Average order value | 6,200 DZD / $48 | **weakest assumption, see Part 5** |
| **COD orders per year** | **25.5 M** | derived |

Sanity checks, all of which hold:

- 25.5 M orders across 200,000 merchants is 128 orders per merchant per year,
  about 11 a month. Right for a long tail of small Instagram sellers.
- 70,000 parcels a day nationally. If Yalidine carries 40%, that is 28,000 a day
  across 160 branches, or 175 per branch. Plausible for a courier branch.
- If the serious 18% of merchants carry 80% of orders, they average 47 orders a
  month, which is consistent with the break-even floor found in Part 2.

**Serviceable market: about 36,000 merchants**, being the 18% with enough volume
to pay for tooling. Not 200,000.

### Sensitivity on average order value

| AOV | Orders per year | Parcels per day |
|---|---|---|
| 5,000 DZD / $38 | 31.6 M | 87,000 |
| 6,200 DZD / $48 | 25.5 M | 70,000 |
| 7,500 DZD / $58 | 21.1 M | 58,000 |

---

## Part 4: Projected usage and revenue

### Revenue per merchant, at 60 orders a month

| Line | Basis | Monthly |
|---|---|---|
| Confirmation | 60 calls at 30 DZD | $13.85 |
| Platform fee | 2,500 DZD, above volume threshold | $19.23 |
| Upsell commission | 15% accept, 65 DZD each | $4.50 |
| **Mature ARPU** | | **$37.58** |

Pricing the call at 30 DZD sits just under the Moroccan anchor of 2.8 dirhams,
roughly 36 DZD.

### Three-year projection

| Scenario | | Year 1 (2027) | Year 2 (2028) | Year 3 (2029) |
|---|---|---|---|---|
| **Bear** | merchants | 300 | 1,000 | 2,500 |
| | ARR | $0.05 M | $0.24 M | $0.75 M |
| **Base** | merchants | 500 | 2,500 | 6,000 |
| | ARR | $0.08 M | $0.84 M | $2.66 M |
| **Bull** | merchants | 800 | 4,500 | 12,000 |
| | ARR | $0.13 M | $1.84 M | $6.48 M |

Year 1 is per-order pricing only, deliberately. The platform fee and upsell
commission arrive in year 2 once the order board and router exist.

Base case year 3 in context:

| Measure | Value |
|---|---|
| Merchants | 6,000, or 17% of serviceable market |
| GMV flowing through | $206 M |
| Share of national COD GMV | 17% |
| Effective take rate | 1.29% |

A 17% share of national volume by year three is aggressive. It is defensible only
because the dinar barrier keeps better-funded foreign entrants out, and because
the only credible local competition is a courier deciding to build it.

### Ceilings

| Revenue pool | Annual |
|---|---|
| Confirmation calling alone | $5.9 M |
| Full stack at 1.0% of COD GMV | $12.2 M |
| Full stack at 1.5% of COD GMV | $18.2 M |
| Full stack at 2.0% of COD GMV | $24.3 M |

**Confirmation calling is too small to be the business.** At $5.9 M for the entire
country it is a customer acquisition wedge, not a destination. The company only
works if it expands into the order board, the router and eventually payment. Any
plan that stops at voice calling caps out under $6 M.

---

## Part 5: What would break this

- **The average order value assumption.** It is derived, not published, and it
  drives the whole order count. Validate it first, from carrier data or a sample of
  merchants, before committing to a plan. Everything downstream moves with it.
- **A courier builds it.** Yalidine already has the merchant relationships, the
  cash flows and the delivery data. It is the single most dangerous competitor and
  it is not foreign, so the dinar barrier does not protect against it. Partner
  early or expect to be copied.
- **Derja speech quality.** Algerian Derja is among the least-resourced Arabic
  dialects. It appears in the multi-dialect Casablanca corpus but has nothing like
  the dedicated datasets Moroccan Darija now has. Expect to build the training set,
  and treat that data as the real asset.
- **Device contraction.** Algerian smartphone shipments fell 28% in the first
  quarter of 2026, and Omdia forecasts a 28% contraction in the ultra-low-cost
  segment across Africa for the year. Merchant-side software is insulated. Any
  consumer-facing surface is not.
- **Regulatory drift.** Merchants need CNRC registration under Law 18-05 to touch
  regulated payment channels. The planned 2026 sandbox helps, but taking payment
  rather than just orchestrating cash is a licensing question, not a product one.
- **The dinar cuts both ways.** The same non-convertibility that keeps Stripe out
  makes it hard to pay foreign infrastructure bills or return capital to outside
  investors. Revenue is collected in dinars and largely has to be spent in dinars.

---

## Bottom line

The wedge is real and pays for itself for any merchant above roughly 20 orders a
month. The wedge alone caps out under $6 M a year nationally, so it has to become
the order board and the courier router to matter. Base case is about $2.7 M of
annual recurring revenue in year three against a serviceable base of 36,000
merchants, and the number to validate before anything else is average order value.
