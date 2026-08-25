#  25(B)lend — Project & Business Model

> Complete architectural, legal, financial, and publisher-aligned blueprint for 25(B)lend, as of 25.08.2026

---

## 1. Executive Summary & Problem Statement

Educational resources have become financially prohibitive. High-demand textbooks routinely cost $40–$60 per digital edition with artificial access expirations. This pricing model forces students into a false binary:
1. **Severe Financial Strain:** Overpaying for temporary access keys that expire at the end of a semester.
2. **Shadow Libraries & Piracy:** Downloading unverified PDFs from illegal repositories, exposing users to security risks while providing **zero revenue** to authors and publishers.

**25(B)lend** establishes a middle ground: an open-source, non-profit Controlled Digital Lending (CDL) infrastructure that guarantees student access, enforces strict legal 1:1 lending ratios, and creates sustainable revenue streams for publishers.

---

## 2. Publisher Value Proposition & Business Mechanics

Instead of fighting content creators, 25(B)lend presents publishers with a secure, highly profitable alternative to shadow libraries:

### Key Advantages for Publishers
* **Piracy-to-Revenue Redirection:** Converts traffic currently lost to shadow libraries (Z-Library, Telegram) into legal, monetisation-ready library interactions.
* **High-Intent Store Funnel ("Skip the Queue"):** When all 1to1(1:1) copies are borrowed, waitlisted users see a direct "Purchase Personal Copy" button. The platform takes **0% affiliate commission**, sending 100% of purchase revenue to the publisher/store.
* **Dual-Stream Monetisation:** Publishers receive full-price upfront sales for perpetual institutional licenses alongside ongoing micro-royalties per borrow event.
* **Zero-Leak Protection:** In-memory WebAssembly execution prevents file downloading, DOM scraping, and PDF redistribution—offering far stronger protection than traditional web readers.
* **Upfront Liquidity:** Community pools crowdfund full perpetual license fees upfront, providing immediate financial returns for creators.
* **Aggregate Learning Analytics:** Publishers(for learning books) receive non-PII engagement metrics (e.g., chapter retention and exercise review counts) to refine future editions without tracking individual student privacy.

###  Operational Table

| Mechanism | Description | Benefit to Publisher | Benefit to Reader |
| :--- | :--- | :--- | :--- |
| **Crowdfunded Pools** | Community pools raise funds to purchase perpetual institutional licenses. | Upfront full-price license sales with immediate liquidity. | Free borrowing of a voted book. |
| **Micro-Royalties** | Micro-payments allocated per borrow event via grants/donations (also & probably some no invasive adds) (also maybe some help from government funds?). | Passive secondary income stream per checkout. | Sustainable library expansion. |
| **Direct Purchase Funnel** | Direct store purchase links for users on borrowing waitlists. | Instant sales conversion with 0% platform fee. | Option to skip queues legally. |

---
## 3. Technical Architecture 

To give publishers total confidence in digital lending, 25(B)lend replaces raw file downloads (PDF/EPUB) with a client-side execution container:
* **Memory-Only Canvas Rendering:** Assets are fetched as encrypted raw bytes, decrypted strictly inside WebAssembly/Service Worker RAM, and drawn directly onto an HTML5 Canvas. No raw media URLs or unencrypted blobs ever leak into the browser DOM.
* **Offline PWA Caching:** Offline reading is supported via Service Workers with ephemeral, self-expiring local decryption keys (e.g., hard 24-hour expiration window requiring periodic check-in).
* **Accessibility Layer:** An invisible Shadow DOM layer overlays the Canvas to provide text nodes for screen readers (NVDA, JAWS, VoiceOver) while enforcing rate limits to block automated scraping.
* **Dual-View Sandbox:** Optimised for language learning and exercise-heavy books, allowing side-by-side rendering of textbooks and workbooks with synced audio playback.

---
## 4. Legal Compliance & Governance

* **Strict 1:1 Lending Ratio:** For every physical or perpetual digital license owned by the community pool, exactly **one user** can borrow and read the digital copy at a time.
* **Copyright Strategy:** We operate under good-faith CDL principles. We actively seek direct publisher agreements for perpetual digital ownership rather than relying solely on fair-use exemptions.
* **Privacy First (Non-PII):** The platform collects **zero Personally Identifiable Information (PII)**. Analytics are aggregated client-side to report usage metrics to authors without tracking student behaviour.
* **Open Source Licensing:** Software is released under the **GNU Affero General Public License v3.0 (AGPL-3.0)** to guarantee that all downstream forks remain free, open, and transparent.

---
## 5. Community & Decision Making

25(B)lend is a community-owned initiative. All technical architectural choices, governance rules, and roadmap priorities are debated publicly in our [GitHub Discussions](https://github.com/25-B-lend/reader/discussions) and tracked via open [GitHub Issues](https://github.com/25-B-lend/reader/issues).

## Goal and Constitution
**Empower the consumer with fair, free access to books, in their most varied forms, without degrading publishers or diminishing creator livelihoods.**
