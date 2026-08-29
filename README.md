# 25(B)lend 

---

## 1. Executive Summary & Quick Overview

Educational resources have become financially prohibitive. High-demand textbooks routinely cost $25–$60 per digital edition. **25(B)lend** is an open-source, non-profit initiative building a client-side WebAssembly reader that enforces strict 1:1 digital lending ratios while establishing sustainable, legal revenue streams for publishers.

> **Looking for our idea, financial, and legal strategy?**  
> Read the complete **[`MODEL.md`](./MODEL.md)** for the complete blueprint 

---

## 2. Core Features & Technical Highlights

* **Memory-Only Canvas Rendering:** Assets are decrypted strictly inside WebAssembly/Service Worker RAM and rendered directly onto an HTML5 Canvas, preventing DOM media leaks and file downloads.
* **Strict 1:1 CDL Engine:** Mathematical enforcement guaranteeing that one acquired license equals exactly one active borrower at a time.
* **Study Sandbox:** Side-by-side view for main textbooks (*Kursbuch*) and workbooks (*Arbeitsbuch*), synchronised audio playback, and private vector annotations.
* **Offline PWA Engine:** Encrypted Service Worker caching with self-expiring local decryption keys.
* **2D Virtual Reading Room:** Lightweight 2D spatial canvas with custom avatars and library tables for real-time peer study.
* **Accessibility Layer:** Invisible Shadow DOM fallback layer for screen readers (NVDA, JAWS, VoiceOver).

---

You don't need to be a software engineer to make a massive impact on 25(B)lend. Building an ethical alternative to textbook piracy requires educators, legal minds, designers, and students alike.



We are actively looking for help across all areas:

* **Developers & Security Engineers:** Help us build the Canvas rendering engine, Wasm decryption pipeline, and PWA caching.

* **Students & Learners:** Test early builds, give UX feedback, and highlight high-demand titles.

* **Educators & Translators:** Help curate open-access materials and localize the interface (i18n).

* **Legal & IP Advisors:** Help draft copyright-compliant 1:1 lending templates for publisher outreach.

* **UI/UX Designers:** Shape the dual-screen study interface and annotation tools.
  
* **Artists/Designers:** To shape how the world sees us. 

* **Idealisers:** Give us your idea/s; all are welcome and pretty much apreciated!





### How to Get Involved

1. Explore open tasks in **[Issues](https://github.com/25-B-lend/reader/issues)**.

2. Jump into **[GitHub Discussions](https://github.com/25-B-lend/reader/discussions)** to share ideas, pitch features, or ask questions.

3. Share the project with anyone passionate about educational and free reading access!





##  A Note on Our Current Stage

25(B)lend is in its early stages. Every issue and feature is meant to be discussed, challenged, and refined by the community before becoming a fixed goal.



Everyone has a voice here:

* **Refining Issues:** Share your thoughts, technical approaches, or critiques directly in the issue comments.

* **Proposing New Ideas:** If you have an idea that isn't covered yet, feel free to open a new Issue or start a Discussion thread.

