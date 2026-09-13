# Competition, and whether to launch

Part four. Research date: September 2026.

---

## Verdict

**No, not as drafted.** The diaspora bill-pay app is already built, by the company
with 41 percent of the market, priced below the margin the model assumed.

Damane Cash was created in 2025 as a subsidiary of Banque Centrale Populaire with an
exclusive focus on Moroccans living abroad. It is a fully digital mobile app
offering money transfers, **bill payments**, cash services and a wallet, at a 0.5
percent transfer fee. That is the prototype in `app/`, shipped a year ago, by the
incumbent, at a lower price than the 0.55 percent spread the model depended on.

This does not mean the research was wrong. It means the specific product drafted in
part four of this work is the wrong entry point, and the honest thing is to say so
before any money is spent.

One gap did open up in the process of checking, and it is a better one. It is in
part three below.

---

## Part 1: Who you would be competing with

### The field

| Player | What it is | Pays family bills? | Price |
|---|---|---|---|
| **Damane Cash** | BCP subsidiary, created 2025, diaspora-only, fully digital | **Yes** | 0.5% |
| **Banque Populaire / Chaabi Bank** | 41% of inbound diaspora transfers. 40+ branches in France, 165 across Europe, 240,000 clients | Yes, in app | Varies |
| **Attijariwafa** | MRE packages, convertible dirham accounts, Wafacash at 2,100 branches | Yes. App pays water, electricity, phone, taxes | Varies |
| **Bank of Africa** | BMCE Diaspora programme | Yes, in app | Varies |
| **Taptap Send** | Diaspora-focused app, 70+ receive countries, Bank of Africa partnership | Transfers, instant to bank | No fee, FX margin |
| **Wise, Remitly, WorldRemit** | Global digital remittance | No | 30–60% below Western Union |
| **Recharge.ma** | Diaspora utility payments for Morocco | Yes | Thin product |
| **Western Union, MoneyGram, Ria** | Legacy agent networks | No | Highest |

Chaabi Bank operates branches in France, Spain, Italy, Belgium and Germany, which
are precisely the five corridors the plan named.

### Why the rail is not a moat either

Fatourati is reachable from virtually every bank's channels. It links 32 banks and
payment providers across more than 70 channels, and had processed over 240 million
payments and 220 billion dirhams by the end of 2025. Any Moroccan bank customer can
already pay a utility bill by entering the reference printed on it.

Bill payment in Morocco is not an unbuilt capability. It is a commodity reachable
from dozens of apps. The part three blocking question, whether a foreign payment
institution can join Fatourati as a paying channel, turns out to be the *second*
problem. The first is that solving it would only get you to parity.

### And the regulator is compressing the margin

Bank Al-Maghrib said in June it was working with the industry to improve efficiency
and transparency in money transfers, expand digital access and reduce transfer
costs. A business whose entire revenue is a 0.55 percent FX spread is on the wrong
side of that.

---

## Part 2: The fair case for launching anyway

Three arguments genuinely cut the other way. They are not enough, but they are real.

**The market is large and accelerating.** Remittances reached 122.02 billion dirhams
in 2025, about $13.4 billion, up 2.6 percent. 2026 is estimated at 138 billion, up
6.2 percent, a record. The first seven months of 2026 came in 8.1 percent ahead of
the year before. This is not a shrinking pool.

**Incumbency did not save the Indian banks.** Aspora is the direct precedent and it
won against Wise, Remitly, Revolut, Western Union *and* Indian banks that already
offered non-resident products. Its stated insight was not a missing feature. It was
that the products existed but nobody found them, because non-residents were using
the same app as residents with no journey built for them. It grew volume 6x in a
year, from $400 million to $2 billion.

**The incumbent's execution is mediocre.** Damane Cash sits at 3.3 stars. That is
the gap a better product normally walks into.

### Why it still is not enough

| Factor | India, where it worked | Morocco |
|---|---|---|
| Corridor size | $100 bn+ a year | $13.4 bn |
| Capital the winner needed | $99 m raised, $500 m valuation | You, remotely |
| Incumbent diaspora-only digital app | None | Damane Cash, since 2025 |
| Price floor when entering | Banks at 2–4% | Already 0.5% |

The market is roughly one eighth the size, the incumbent has already built the
diaspora-only digital product India's banks never did, and the price floor is
already at the level Aspora had to fight *to*. A well-funded team could still take
share on execution. A solo remote founder undercutting 0.5 percent on a $13 billion
market cannot.

---

## Part 3: The gap that actually opened

Checking the competition surfaced something better, and it is the one thing all of
that money cannot currently do.

**Only about 10 percent of the $13.4 billion goes to productive investment.** The
rest is household consumption, savings, and property. Of the investment that does
happen, **70 percent goes into residential property**, chosen because it is
perceived as safe, tangible and manageable from a distance.

The barriers named are not financial. They are operational:

- The difficulty of resolving administrative or technical problems at a distance
  without reliable local support, described as a particularly costly obstacle.
- A fragmented land tenure system with varied legal statuses, access barriers and
  opaque availability.
- Trust, including hesitancy about sending money through banks at all.

The Moroccan government has said explicitly that it wants to shift the relationship
from financial transfers to productive investment.

So the real unserved job is not *moving* the money. It is **owning and running
something in Morocco while living in Lyon**: the syndic fees, the property tax, the
caretaker, the contractor who needs paying and supervising, the rental, the
paperwork, the title. Hundreds of thousands of diaspora families already own
property there and manage it over WhatsApp and family favours.

That is a high-value, high-willingness-to-pay problem with no incumbent, and the
transaction sizes are orders of magnitude above a 187-dirham electricity bill.

### The same tension, again

The hard part of that product is "reliable local support," which is exactly what a
remote founder cannot supply. The software and coordination layer is remote. The
trusted feet on the ground are not.

This is the third time this constraint has bitten in this research. It is the
central problem, not an incidental one.

---

## Where this leaves the whole body of work

| Opportunity | Demand evidence | Remote-buildable | Contested |
|---|---|---|---|
| Algeria COD merchant stack | **Strongest found.** Two native teams building it in public | No. Merchants cannot pay a foreign company | Lightly, and only locally |
| Maghreb diaspora bill-pay | Real but served | Yes | **Heavily. Market leader shipped it in 2025** |
| Diaspora property and admin management | Strong and specific | Partly. Needs local execution | **No incumbent found** |
| Pakistan or Philippines COD tooling | Strong | Mostly | Yes. One player spans seven markets |
| Voice-first layer for non-readers | Strong | Yes | No, but hard to monetise alone |

Everything genuinely uncontested needs someone on the ground. Everything
buildable purely remotely is already contested. That is the finding, and no amount
of further desk research will dissolve it.

## Recommendation

Pick which constraint to relax. There are only two honest options.

**Relax remote-only.** Take the Algeria cash-on-delivery stack with an Algerian
co-founder who owns the local entity and collections. It has the best demand
evidence in this entire body of research, two teams are validating it in public
right now, and the dinar keeps every foreign competitor out. You own the product,
they own the ground.

**Relax the market.** Go at diaspora property and administration management, which
has no incumbent and much larger transaction values, and solve the local-support
problem by partnering with an existing Moroccan property or legal services firm
rather than hiring.

**Do not** launch the bill-pay app as drafted. It is a worse version of a product the
market leader already ships at a price you cannot beat.

### Before deciding, two cheap checks

1. **Download Damane Cash and try to pay a bill for someone else.** Fifteen minutes.
   If it turns out its bill payment only covers the account holder's own bills and
   not a relative's, the wedge is narrower than this assessment assumes and worth
   re-examining. My sources describe the feature but not that distinction.
2. **Talk to ten diaspora property owners.** Ask what they paid someone to handle
   in Morocco last year, and what went wrong. Willingness to pay for the part three
   opportunity is untested, and nothing in this research establishes it.

---

## Sources

Competitive landscape from Wafir.ma's diaspora observatory and transfer guides,
Bank of Africa's Taptap Send announcement, Attijariwafa Bank's own personal and
diaspora banking pages, Paysend's Damane Cash partnership release, and Damane Cash's
Google Play listing. Remittance figures from Morocco World News reporting on Bank
Al-Maghrib data. Investment share and barriers from Ecofin Agency, The North Africa
Post and Bladi. Fatourati scale from Morocco World News and CMI coverage. Aspora
comparison from TechCrunch, Sequoia Capital and YourStory.
