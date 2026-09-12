# Dari: app draft

A phone app for the Maghreb diaspora to pay bills back home and see the receipt.
This is Shape A from `../research/remote-build-and-other-markets.md`, the only one
of the three candidate shapes that can be run entirely remotely.

`dari-prototype.html` is a clickable draft. Open it in a browser. It has a platform
toggle for iPhone and Android chrome, a French and Arabic language toggle, and a
working payment flow from bill to receipt.

---

## Why this and not the merchant tool

The Algerian cash-on-delivery stack is a web dashboard for merchants who cannot pay
a foreign company. This is a consumer app for senders in Europe who can. The sender
is billed in euros on ordinary European card rails, so the dirham and the dinar
never touch revenue.

## What the app does

| Screen | Job |
|---|---|
| Home | What is outstanding for family right now, not a blank send box |
| Person | One relative, their bills, pay everything at once |
| Pay | Amount in dirhams, cost in euros, rate and route shown before confirming |
| Receipt | Proof it was paid, with a reference, shareable to family on WhatsApp |
| Repeats | Auto-pay each month with a cap that stops an unexpected jump |
| Activity | History, and fees paid to date |

The product idea in one line: the sender is not buying a transfer, they are buying
**certainty that the thing got paid**. Cash transfer is already cheap and
competitive. Proof of payment is not.

## Design decisions worth keeping

- **Outstanding bills lead the home screen.** Every competitor opens with an amount
  field. Opening with what the family actually owes is the whole differentiator.
- **A cap on recurring payments.** The fear that stops people automating is a bill
  jumping unexpectedly. The cap removes it.
- **Both rates shown.** Today's rate and the mid-market rate sit side by side on the
  profile screen, with the margin stated. Revenue comes from the spread, not fees,
  matching the model the Indian-diaspora incumbent proved.
- **Cash pickup as the honest fallback.** Not every payee is on the bill network. A
  pharmacy account is not. The app says so and routes to cash instead of failing.
- **Arabic is a first-class layout, not a translation.** The prototype ships a real
  Arabic typeface and right-to-left text for the strings a recipient-facing screen
  would carry.

## Stack

**React Native with Expo.** One codebase for both stores. The screens are lists,
forms and a confirmation flow, with no heavy graphics or platform hardware use, so
there is no case for going native twice. Expo builds both binaries in the cloud, so
shipping to the App Store does not require a Mac, which matters for a remote team.

Platform differences are chrome, not logic: iOS centres the title and labels the tab
bar, Android left-aligns the title and puts a pill behind the active tab icon, and
corner radii differ. A handful of `Platform.select` calls covers it.

## Store requirements

| Item | Apple App Store | Google Play |
|---|---|---|
| Developer account | $99 a year, plus a registered legal entity for a finance app | $25 one-off |
| Finance category | Must show the licensed entity operating the service | Financial services declaration and proof of licence |
| First review | Several rounds likely, money apps get scrutinised | Faster, but the finance declaration gates release |
| Build machine | Not needed with Expo cloud builds | Not needed |

## Integrations

| Layer | Provider | Status |
|---|---|---|
| Bill payment | Fatourati, Morocco's shared network, 32 banks and payment providers, 70+ channels, REST API | **Open question, see below** |
| Mobile top-up | Commercial airtime APIs cover Maroc Telecom, Orange and inwi | Available today |
| Cash pickup | Wafacash, Cash Plus, Barid Cash | Available via partners |
| Sender payments | European card acquiring in euros | Available today |
| Licence | Registered agent of an authorised payment institution | 4 to 12 weeks |

Fatourati had handled over 240 million payments and 220 billion dirhams by the end
of 2025. It covers utilities and school fees, which is why school fees appear in the
prototype.

## The blocking question

Fatourati's API is documented for **billers** publishing invoices, and payments are
collected through its Moroccan bank and wallet channels. Whether a foreign payment
institution can join as a **paying** channel is the thing the entire product rests
on, and it could not be confirmed from public sources.

Settle this with the processor before writing application code. If the answer is no,
the route in is partnering with a Moroccan licensed institution that is already a
channel. That changes the company structure but not the app.

## Competition

An incumbent already sells diaspora utility payments for Morocco covering the
national utility and the Casablanca distributor, accepting international cards and
PayPal. It is small and the experience is thin, which is the opening. It also means
the idea is validated and you are not first.

## Build order

1. Confirm the Fatourati channel question. Everything else is wasted effort until
   this is answered.
2. Start agent registration with a sponsoring payment institution in parallel, since
   it takes 4 to 12 weeks.
3. Ship top-ups only, as a standalone app. Airtime APIs are available now and need
   no bill-network access, so this validates acquisition and sender billing while
   the licence and the Fatourati answer are pending.
4. Add bill payment for one biller in one city. Casablanca electricity and water is
   the highest-frequency, lowest-value, most habitual bill.
5. Add recurring payments with caps, then school fees, then the second country.

Step 3 is the real risk reducer. It is a shippable app with revenue that does not
depend on the blocking question.

## Numbers used in the prototype

Rate of 10.85 dirhams to the euro against a mid-market rate of 10.91, a margin of
0.55 percent. A small apartment's monthly electricity bill of 150 to 200 dirhams.
Operator shares of 43, 34 and 22 percent for Maroc Telecom, Orange and inwi. All
names, references and people in the prototype are invented examples.
