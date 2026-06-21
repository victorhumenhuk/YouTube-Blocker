# Decision Ledger — YouTube-Blocker

Durable record of the significant decisions made in this repository and the reasoning behind them.

- **Confirmed** decisions are human-reviewed and binding. This section is maintained by the repository owner; the automated decision-ledger pass never edits it.
- **Inferred** decisions are hypotheses proposed automatically from the code, commit history, and any agent instructions (CLAUDE.md / AGENTS.md). They are **not binding** until the owner moves them into Confirmed.

## Confirmed

_None yet. Merge a proposal from Inferred to confirm it._

## Inferred (proposed — awaiting confirmation)

> Every item below is a hypothesis generated automatically on 2026-06-21. Where the rationale could not be recovered from the available evidence it is marked "rationale unknown — please supply".

### [hypothesis] Repository scope is a public support / documentation page, not application source
- **Decision:** This repository contains only Markdown documentation (`README.md`, `SUPPORT.md`) serving as the public-facing App Store support page for the YouTube Blocker app; the actual application source lives in a separate repository (`Youtube-Channel-Blocker`).
- **Rationale (hypothesis):** App Store listings require a reachable support URL; a small dedicated docs repo provides a stable public page while keeping the app source separate. The README and SUPPORT both link out to the separate `Youtube-Channel-Blocker` repo for project files and privacy policy.
- **Evidence:** Commit `d7a3db0` ("Add App Store support page"); only files present are `README.md` and `SUPPORT.md`; `README.md` lines 30-35 and 26-28 link to `https://github.com/victorhumenhuk/Youtube-Channel-Blocker`.
- **First observed:** `d7a3db0` (2026-04-26)

### [hypothesis] GitHub Issues is the sole support channel
- **Decision:** User support requests are routed exclusively through GitHub Issues, with a defined intake template (device/OS version, Safari version, description, YouTube page type).
- **Rationale (hypothesis):** rationale unknown — please supply
- **Evidence:** `SUPPORT.md` lines 3-5; `README.md` lines 5-16 (intake checklist including Home, Search, Video, Shorts, Channel page types).
- **First observed:** `d7a3db0` (2026-04-26)

### [hypothesis] Privacy-by-design: local-only block list, no data collection, no accounts
- **Decision:** The block list is stored locally on the user's device; the app collects no personal data, creates no accounts, and never sends the block list to a server.
- **Rationale (hypothesis):** Documented as a deliberate privacy posture for the product; keeping data on-device avoids server infrastructure and data-handling obligations.
- **Evidence:** `README.md` line 20 ("The block list is stored locally on your device."); `README.md` lines 22-24 ("does not collect personal data, create accounts, or send your block list to a server.").
- **First observed:** `d7a3db0` (2026-04-26)

### [hypothesis] Target platform is Safari on Apple devices
- **Decision:** YouTube Blocker is positioned as a Safari extension / Apple App Store app, with support intake specifically requesting the Safari version.
- **Rationale (hypothesis):** rationale unknown — please supply
- **Evidence:** `README.md` line 14 ("The Safari version you are using."); commit `d7a3db0` message "Add App Store support page".
- **First observed:** `d7a3db0` (2026-04-26)

### [hypothesis] Product naming standardized to "YouTube Blocker"
- **Decision:** The support page and product references were renamed/standardized to "YouTube Blocker" (distinct from the source repo name "Youtube-Channel-Blocker").
- **Rationale (hypothesis):** rationale unknown — please supply
- **Evidence:** Commit `5c15496` ("Rename support page to YouTube Blocker"), touching `README.md` and `SUPPORT.md`.
- **First observed:** `5c15496` (2026-04-26)

---
*Decision-ledger automated pass. Operation: Bootstrap. Last reflection: commit `5c15496` (2026-06-21). Decisions above are AI-inferred hypotheses; nothing is binding until merged into Confirmed.*
