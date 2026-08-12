<h1 align="center">Andy Tran</h1>

<p align="center">
  <b>I run operations at an auto shop and build the software that runs it.</b><br>
  Not a side project. It's open at 8am and the software has to work.
</p>

<p align="center">
  <a href="https://www.andytran.tech"><b>andytran.tech</b></a> &nbsp;·&nbsp;
  <a href="https://acautoclinic.com"><b>A&amp;C Auto Clinic</b></a> &nbsp;·&nbsp;
  San Francisco
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/Postgres-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="Postgres">
  <img src="https://img.shields.io/badge/Drizzle-C5F74F?style=flat-square&logo=drizzle&logoColor=black" alt="Drizzle">
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel">
  <img src="https://img.shields.io/badge/Fly.io-24175B?style=flat-square&logo=flydotio&logoColor=white" alt="Fly.io">
  <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude API">
</p>

---

### What I'm building

**Duyna** — the operating system for an independent repair shop. Estimates, parts, bay tracking, payments, receivables, customer portal. It replaces a per-seat SaaS the shop was renting, and it runs in production every day at a real shop with real money moving through it.

**Yew** — the payments layer underneath. A multi-tenant Next.js app that drives PAX A80 card terminals over POSLink: browser → Vercel → a Fly.io WebSocket gateway → a Raspberry Pi on the shop's LAN → the terminal. Money is integer cents, card numbers never touch the database, every mutation is idempotent.

The interesting part isn't the stack. It's that I work the front desk, so I find out the same day when something I shipped makes a service advisor's job worse.

### Agent evaluation

I also write adversarial evaluations for coding agents. The work is building tasks a frontier model reliably fails, that still have objective tests any correct solution passes. Both halves are the hard part: make it too easy and it grades nothing, make it ambiguous and it grades the wrong thing.

What it's taught me, and what feeds back into the code above: models fail in specific, reproducible ways, and the failure you assumed is usually not the failure you get. So I review model output the same way I review my own diffs, with a second model that has different blind spots.

### Before this

**Supplyframe** (acquired by Siemens) — core pricing engine for an enterprise CPQ platform. Quoting rules, calculations, and configuration workflows across 50K+ SKUs, plus query tuning on catalog pipelines handling 200K+ records.

**Red Bull Media House** — sole engineer on the ad-serving microservice for ServusTV. Third-party ad APIs (VAST/VPAID), insertion logic for pre-roll, mid-roll, and companion formats across 23 device types, and live/VOD playback infrastructure (HLS/DASH) streaming to 2M+ devices.

Alongside that I built and launched **ScoreZero**, an AI credit-recovery product for post-bankruptcy users.

### How I work

- **Reproduce it end-to-end before fixing it.** If I can't trigger the bug the way a user hit it, I haven't found it yet.
- **Fail closed.** A gate that errors open isn't a gate. Timeouts, unparseable output, and missing config all count as "blocked."
- **Cross-model review.** A second model with different blind spots reviews what the first one wrote before it merges.
- **Boring where it counts.** Integer cents, explicit migrations, no clever money math.

### A note on what's public here

Most of what I build is private, because it's the operating software for a business that's still running on it. What's pinned below is the public slice: agent orchestration, some full-stack work, and the Windows bridge installer that ships alongside the payments stack.

If you want to talk about the private work, the fastest path is <a href="https://www.andytran.tech">andytran.tech</a>.
