# 25(B)lend — Project & Business Model

> Complete architectural, legal, financial, and publisher-aligned blueprint for 25(B)lend, as of **__29.08.2026__**

---

## 1. Executive Summary & Problem Statement

Educational resources have become financially prohibitive. High-demand textbooks routinely cost $25–$60 per digital edition with artificial access expirations. This pricing model forces students into a false binary:
1. **Severe Financial Strain:** Overpaying for temporary access keys that expire at the end of a semester.
2. **Shadow Libraries & Piracy:** Downloading unverified PDFs from illegal repositories, exposing users to security risks while providing **zero revenue** to authors and publishers.

**25(B)lend** establishes a middle ground: an open-source, non-profit Controlled Digital Lending (CDL) infrastructure that guarantees student access, enforces strict legal 1:1 lending ratios, and creates sustainable revenue streams for publishers.

---

## 2. Publisher Value Proposition & Business Mechanics

Instead of fighting content creators, 25(B)lend presents publishers with a secure, highly profitable alternative to shadow libraries:

### Key Advantages for Publishers
* **Piracy-to-Revenue Redirection:** Converts traffic currently lost to shadow libraries (Z-Library, Telegram) into legal, monetisation-ready library interactions.
* **High-Intent Store Funnel ("Skip the Queue"):** When all 1to1(1:1) copies are borrowed, waitlisted users see a direct "Purchase Personal Copy" button. The platform takes **0% affiliate commission**, sending 100% of purchase revenue to the publisher/store.
* **Multi-Stream Monetisation:** Publishers receive full-price upfront sales for perpetual institutional licenses alongside ongoing micro-royalties per borrow event.
* **Zero-Leak Protection:** In-memory WebAssembly execution prevents file downloading, DOM scraping, and PDF redistribution. Therefore, it offers far stronger protection than traditional web readers.
* **Upfront Liquidity & Crowdfunding:** Community pools and our annual Pixel Canvas crowdfund full perpetual license fees upfront, providing immediate financial returns for creators.
* **Aggregate Learning Analytics:** Publishers (especially for courseware & learning materials) receive non-PII engagement metrics (e.g., chapter retention and exercise review counts) to refine future editions without tracking individual student privacy.

### Operational Table

| Mechanism | Description | Benefit to Publisher | Benefit to Reader |
| :--- | :--- | :--- | :--- |
| **Crowdfunded Pools & Pixel Canvas** | Community pools raise funds via Open Collective and an annual 500×500 Pixel Canvas (€0.10/px, frozen annually into a Founders Gallery). | Upfront full-price license sales with immediate liquidity. | Free borrowing of a community-voted book for life. |
| **Micro-Royalties** | Micro-payments per borrow event via grants/donations, optional non-intrusive sponsorships, or public/government funds. | Passive secondary income stream per checkout. | Sustainable library expansion and new title additions. |
| **Direct Purchase Funnel** | Direct store purchase links embedded into waitlist screens for queue-skipping. | Instant sales conversion with 0% platform fee. | Option to skip queues legally and support authors directly. |
| **Financial Reserve Cap & Surplus Trigger** | Operations adhere to a 150% maximum retention cap (100% base + 20% buffer + 30% emergency reserve). All excess revenue is automatically redistributed. | Transparent non-profit partner operating with long-term financial stability. | Guarantee that funds directly support education (70% surplus buys new books, 30% donated to literacy non-profits). |

---

## 3. Technical Architecture 

To give publishers total confidence in digital lending, 25(B)lend replaces raw file downloads (PDF/EPUB) with a client-side execution container:
* **Memory-Only Canvas Rendering:** Assets are fetched as encrypted raw bytes, decrypted strictly inside WebAssembly/Service Worker RAM, and drawn directly onto an HTML5 Canvas. No raw media URLs or unencrypted blobs ever leak into the browser DOM.
* **Offline PWA Caching:** Offline reading is supported via Service Workers with ephemeral, self-expiring local decryption keys (e.g., hard 24-hour expiration window requiring periodic check-in).
* **Accessibility Layer:** An invisible Shadow DOM layer overlays the Canvas to provide text nodes for screen readers (NVDA, JAWS, VoiceOver) while enforcing rate limits to block automated scraping.
* **Dual-View Sandbox:** Optimised for language learning and exercise-heavy books, allowing side-by-side rendering of textbooks (*Kursbuch*) and workbooks (*Arbeitsbuch*) with synced audio playback.
* **2D Virtual Reading Room (Spatial Study):** A lightweight 2D spatial canvas allowing users to customise an avatar and sit at virtual library tables (1-person focus desks, 2-person peer seats, and 4-to-8-person group tables) to study together in real time and share notes.

---

## 4. Legal Compliance & Governance

* **Strict 1:1 Lending Ratio:** For every physical or perpetual digital license owned by the community pool, exactly **one user** can  read the digital copy at a time.
* **Copyright Strategy:** We operate under good-faith CDL principles. We actively seek direct publisher agreements for perpetual digital ownership rather than relying solely on fair-use exemptions.
* **Privacy First (Non-PII):** The platform collects **zero Personally Identifiable Information (PII)**. Analytics are aggregated client-side to report usage metrics to authors without tracking student behaviour.
* **Ethical Capital Governance:** Operations strictly adhere to the 150% financial reserve cap. Capital accumulation above 3–6 months of emergency operating costs is forbidden, triggering automatic allocations to buy book licenses (70%) and support partner literacy charities (30%).
* **Open Source Licensing:** Software is released under the **GNU Affero General Public License v3.0 (AGPL-3.0)** to guarantee that all downstream forks remain free, open, and transparent.

---

## 5. Ideal Roadmap
---
### Phase 1: Engine Core & Technical PoC *(Current)*
**Goal:** Validate zero-leak Wasm rendering and build the basic reading interface using Open Educational Resources (OER).

* **Core Wasm Engine:** Implement client-side dynamic page decryption inside WebAssembly and Service Worker RAM.
* **Canvas Renderer:** Build a memory-only HTML5 Canvas drawing pipeline (zero unencrypted blobs or media URLs exposed to DOM).
* **Accessibility Base Layer:** Integrate invisible Shadow DOM fallback layer for screen readers (NVDA, JAWS, VoiceOver).
* **Dual-View Study Sandbox:** Develop side-by-side rendering layout for textbooks and workbooks with synced audio playback.
* **Repository Governance:** Establish complete community contributor documentation (`README.md`, `MODEL.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`).

---

### Phase 2: Financial, Legal & Community Infrastructure
**Goal:** Deploy transparent non-profit funding mechanics and standardise publisher-friendly CDL contracts.

* **Open Collective Host:** Set up transparent fiscal hosting and public ledger tracking.
* **Annual Pixel Canvas (500×500):** Launch the 250,000-pixel crowdfunding grid (€0.10/px in 10×10 blocks) with automated annual archiving to the Founders Gallery.
* **Surplus Logic Automation:** Code open ledger triggers enforcing the 150% financial reserve cap and automatic redistribution (70% book licenses / 30% literacy charities).
* **Standardized 1:1 CDL Templates:** Draft copyright-compliant publisher agreements guaranteeing technical 1:1 lending ratios.
* **Offline PWA Security:** Implement Service Worker local caching with 24-hour self-expiring decryption keys.

---

### Phase 3: Spatial UX & Public Beta Launch
**Goal:** Introduce community study features and launch the first public book lending pilot.

* **2D Virtual Reading Room:** Implement WebSocket-powered spatial study canvas featuring customizable 2D avatars, focus desks, and peer study tables (2–8 seats).
* **Publisher Direct-Store Funnel:** Integrate "Skip the Queue / Buy Copy" referral links on waitlist screens with 0% platform commission.
* **Annotated Vector Layer:** Add private, local account drawing and note-taking overlays across canvas frames.
* **Public Pilot Launch:** Deploy first library pool containing community-voted OER and licensed educational titles.

---

### Phase 4: Publisher Integration & NGO Formalisation
**Goal:** Transition platform governance into a registered non-profit NGO and scale institutional adoption.

* **Publisher Analytics Dashboard:** Deploy privacy-focused, non-PII aggregate telemetry (chapter retention, exercise review metrics) for content creators.
* **Institutional API:** Build secure connector protocols for university and municipal library software (ILS/LMS integration).
* **NGO Formalisation:** Establish legal non-profit entity status governed by open-source community bylaws.
* **Global License Pools:** Expand the perpetual digital license acquisitions.




## 6. Community & Decision Making

25(B)lend is a community-owned initiative. All technical architectural choices, governance rules, and roadmap priorities are debated publicly in our [GitHub Discussions](https://github.com/25-B-lend/reader/discussions) and tracked via open [GitHub Issues](https://github.com/25-B-lend/reader/issues).

## Goal and Constitution

**Empower the consumer with fair, free access to books, in their most varied forms, without degrading publishers or diminishing creator livelihoods.**
