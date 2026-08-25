# 25(B)lend Core Reader

> Reclaiming educational access. An open-source, non-profit Controlled Digital Lending platform for textbooks.

---

## Our ideals:
Modern education and reading are locked behind an unsustainable paywall. High-demand textbooks routinely cost $40–$60 per edition, while traditional libraries lack modern digital lending infrastructure for interactive courseware. This leaves students and readers trapped between financial strain and pirated PDFs, leaving publishers with zero revenue and students with zero protection.

**25(B)lend** is trying to bridge this gap. We are building a non-profit, zero-leak Controlled Digital Lending (CDL) web platform designed to empower learners, defend user and customer rights, and establish a sustainable, 1:1 legal model with publishers.

---

## The Plan & Roadmap

* **Phase 1: Reader Engine PoC (Current)**  
  Develop the core WebAssembly + Canvas web reader using Open Educational Resources (OER) and Creative Commons content to validate memory-only security and performance.
* **Phase 2: Legal & Crowdfunding Engine**  
  Finalise the transparent Open Collective financial setup and draft the 1:1 institutional licensing framework for publisher partnerships.
* **Phase 3: Publisher Onboarding & Platform Launch**  
  Roll out community-funded license purchases, micro-royalty tracking, and publisher store funnels alongside the dual-view study sandbox.

---

## Core Features
* **Memory-Only Canvas Rendering:** Dynamic page rendering via HTML5 Canvas & WebAssembly (Wasm) without exposing raw file assets to the browser DOM or local disk.
* **Strict 1:1 CDL Ratio:** Mathematical enforcement ensuring one acquired license equals one active borrower at a time.
* **Study Sandbox:** Side-by-side view (Textbook + Workbook), private vector annotation layers that stay in your account, and timestamp-synced audio playback.
* **Ethical Monetisation:** Crowdfunded license pools, passive micro-royalties (pay-per-borrow), and direct publisher purchase funnels for zero wait-times.
* **Privacy First:** Non-PII, aggregate learning analytics provided to publishers without compromising student privacy.

---

## Tech Stack
* **Core Engine:** WebAssembly (Wasm) + HTML5 Canvas
* **Offline Storage:** Encrypted Service Workers (PWA) with self-expiring decryption keys
* **Accessibility:** Shadow DOM fallback layer for screen readers (NVDA/JAWS)

---

## Everyone is Welcome!

You don't need to be a software engineer to make a massive impact on 25(B)lend. Building an ethical alternative to textbook piracy requires educators, legal minds, designers, and students alike.

We are actively looking for help across all areas:
* **Developers & Security Engineers:** Help us build the Canvas rendering engine, Wasm decryption pipeline, and PWA caching.
* **Students & Learners:** Test early builds, give UX feedback, and highlight high-demand titles.
* **Educators & Translators:** Help curate open-access materials and localize the interface (i18n).
* **Legal & IP Advisors:** Help draft copyright-compliant 1:1 lending templates for publisher outreach.
* **UI/UX Designers:** Shape the dual-screen study interface and annotation tools.
* **Idealisers:** Give us your idea/s; all are welcome and pretty much apreciated!


### How to Get Involved
1. Explore open tasks in **[Issues](https://github.com/25-B-lend/reader/issues)**.
2. Jump into **[GitHub Discussions](https://github.com/25-B-lend/reader/discussions)** to share ideas, pitch features, or ask questions.
3. Share the project with anyone passionate about educational and free reading access!
