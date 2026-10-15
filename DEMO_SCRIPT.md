# CLOTHER — Demo Script (~7 minutes + Q&A)

**Product:** Clother, demonstrated with independent fashion house **Dej. by Ayodeji** (bespoke formalwear).
**Live demo:** https://timiojo.github.io/clother-demo/demo-prototype.html
**Scored on:** problem definition · solution quality · technical execution · UX · business viability · presentation.
**Rule of the demo:** narrate the *customer*, click the *proof*. Never describe a screen you aren't showing.

---

## 0:00–1:00 — PROBLEM DEFINITION (say it plainly)

> "Commissioning a custom outfit today runs on DMs, voice notes, and bank transfers.
> The customer can't compare, can't see what a quote includes, and can't tell what stage
> their piece is at. The designer — usually a one-person business — loses enquiries to
> admin: scattered chats, informal quotes, chasing deposits.
>
> Clother puts the whole commission in one place: discover, brief, consult, quote,
> pay, and track — while the designer keeps full control of their craft, pricing,
> materials, and delivery."

**Show:** Home screen. Point at services, portfolio, review — "everything a stranger needs to trust a studio."

## 1:00–2:30 — SOLUTION QUALITY, part 1: request → project room (click through)

1. **Services → Request this** — "Structured brief, not a DM: garment type, occasion, budget, deadline, notes, reference images."
2. Fill 2 fields live (occasion + notes), **Send request** — project room opens.
3. **Chat tab** — send a message; the studio reply appears. Say: *"Every decision is timestamped against the project — no 'but I said on WhatsApp.'"*
4. **Booking tab** — book a slot. Say: *"Online or in-person, the studio's real availability with notice periods. And a booking is never confused with a production order."*

## 2:30–4:30 — SOLUTION QUALITY, part 2: the money moment (your strongest 2 minutes)

1. **Quote tab** — pause. Let the invoice layout land.
   > "This is the commercial record: itemised scope, exclusions, payment schedule,
   > cancellation terms, expiry. The customer accepts explicitly — chat alone can never
   > silently change the price. Every revision is versioned."
2. Point at the policy block: *"Terms visible before a kobo or penny moves."*
3. **Accept & pay deposit** → mock Flutterwave screen → **Pay now**.
   > "One provider for Nigeria and the UK — cards, transfers. Deposit now, balance on
   > approval. No escrow theatre, no commission math: studio money, settled direct."
4. Back in **Progress tab**: *"Fabric, measurements, production — visible without a single 'any update??' message."*

## 4:30–5:30 — TECHNICAL EXECUTION (one breath, no jargon spiral)

> "Responsive web app — one codebase, no app-store gate. Local Postgres with a typed
> schema, Better Auth with customer/admin roles, Cloudflare R2 for files with
> quarantine-then-promote scanning, ZeptoMail for transactional mail, Flutterwave
> behind a provider interface so the studio is never locked in. Webhooks verified,
> payments idempotent — replay an event five times, charge once. Everything auditable:
> quote acceptance, refunds, admin actions."

Drop one line only if asked: *"Monolith first, modular folders — multi-staff later needs no rewrite."*

## 5:30–6:15 — UX (show, don't claim)

- Scroll the quote: *"Invoice-grade typography, 44-pixel targets, readable on a Tecno on 3G."*
- Chat + status pills: *"A customer always knows the answer to 'where is my dress?' — Awaiting, In progress, Approval, Done."*
- Micro-labels, plain English, no marketplace jargon. *"Designed from the studio's own invoice — the brand they already trust."*

## 6:15–7:00 — BUSINESS VIABILITY + CLOSE

> "One designer, two markets — UK and Nigeria, GBP and NGN kept distinct, unsupported
> routes blocked instead of failed. Revenue is direct: consultations plus deposits and
> balances, with refunds that reconcile. Unit economics are simple because there's no
> marketplace commission to fund. Growth is referrals: every existing client gets an
> invite link that onboards them into a project in one tap — and verified reviews only
> come from real paid work, so trust compounds.
>
> Thank you for trusting us with your occasion."

**Hold the review screen. Stop. Take questions.**

---

## Q&A prep (likely)

- *"Why not native apps?"* — Responsive web covers both markets on day one; store review + installs kill conversion for occasional commissions. Revisit on retention data.
- *"Why Flutterwave, not Stripe?"* — Single dashboard for GBP + NGN; interface keeps a second provider addable without rewriting checkout.
- *"Refunds on custom pieces?"* — Policy set by the studio inside legal minimums, stored per quote version; provider-supported refunds only; statutory rights never overridden.
- *"Privacy of measurements/photos?"* — Private by default, short-lived signed URLs, project members + authorised staff only.
- *"What if the designer hires help?"* — Admin already splits Designer vs Support types; least privilege from day one.
- *"Scale?"* — Monolith + Postgres handles a studio's volume for years; files and mail are already on managed infrastructure.

## If the demo breaks

1. Internet dies → open the local file `demo-prototype.html` (works fully offline).
2. Wrong tap → top-left **Clother** logo always returns home; tabs never lose state.
3. Payment mock stalls → say *"sandbox latency — the redirect verification is the point"* and move to Progress.
