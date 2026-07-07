# PHTC — Shared Context & Handoff

Single source of truth shared between two Claude workspaces:

- **Claude Code** (desktop): builds and edits the website, pushes to the live site. Reads/writes here via git.
- **Browser Claude** (phone/web): brainstorming and wordsmithing the documents (constitution, bylaws, narrative). Reads this file by URL.

Keep this file to **notable points**, not full transcripts. Whoever edits, add a line to the Changelog with your name and the date.

> **This repo is PUBLIC.** Do not put personal contact details, steward emails, the zone contact map, or internal people-strategy here. Those live only in Claude Code's private memory.

## How to update this file
- **Claude Code / Josh:** edit and commit directly.
- **Browser Claude:** you cannot commit. To propose a change, output a clearly labelled block headed `CONTEXT.md update — <date>` containing the exact text to add or replace, and Josh will paste it in (or open a PR).

## Naming & style conventions (apply to all PHTC copy)
- Official name: **Port Hills Trails Collective** (plural "Trails"). Acronym: PHTC.
- Do **not** append "Incorporated" in public-facing copy yet. PHTC is not incorporated. Two live formation paths, decision pending due diligence: (1) transform Canterbury Mountain Bike Club into PHTC at CMBC's AGM (~Aug–Sep 2026), or (2) incorporate fresh as a new org if due diligence gives reason not to reuse CMBC. Avoid asserting either as settled. Use "forming from Canterbury Mountain Bike Club" only when the transform path is being described specifically; otherwise "in formation".
- **No em-dashes** in Josh's copy. Use commas, colons, or periods.
- **US spelling** (organize, recognize, finalize, center).
- "Society" is used in the founding narrative to mean the intended entity; acceptable in that forward-looking document.

## Current status
_As of 2026-07-07:_
- **Website:** live at https://phtc.org.nz. Cloudflare Pages, auto-deploys on push to the private `phtc-site` repo. Pages: home + founding narrative.
- **Founding narrative:** now titled "Founding Narrative & Guiding Principles" (was "Statement of Principles"). Canonical text mirrored in `narrative.md` (this repo). **The live site still shows the old title and old "Riding Public Representative" wording — needs a swap to match.**
- **Constitution:** draft **v1.9** (up from v1.7). Full text now mirrored in `constitution.md`. Still pending: legal review, and the 27 July financials decision on the CMBC transformation path (clauses marked `[CMBC-TIED]` toggle on that decision).
- **Bylaws:** drafted, **v1.2**. Full text now mirrored in `bylaws.md`. Dollar figures, weightings, and thresholds are starting points, not final.
- **Home page menu:** hamburger with How can I help, Log volunteer hours (Google Form), Contact (email), Donate (placeholder; Hivepass memberships open 16 July 2026).
- **Formation:** two candidate paths (see conventions above): transform CMBC, or fresh incorporation. Not yet decided.
- **LMTBC holding vessel:** Lyttelton MTB Club Inc (a separate, already-incorporated club) is being used as an interim signup vessel ahead of PHTC's incorporation. This is orthogonal to the formation-path choice. People who join now transfer into PHTC once it exists, whichever path forms it.
- **LMTBC SGM:** called for Thu 16 July 2026, 7pm, Eruption Brewing. Two motions: (1) establish a $25/yr non-voting "Supporting Rider" membership class via Hivepass, alongside the existing $20 lifetime voting membership; (2) statement of intent to affiliate with PHTC once PHTC is formally established (intent only, no funds committed). Supporting Riders carry forward into PHTC's own supporting-rider class.
- **Naming flag:** the v1.9 narrative draft's title now reads "Port Hills Trails Collective Incorporated," but the naming convention above says not to append "Incorporated" in public-facing copy yet since PHTC isn't incorporated. This wasn't reconciled in the v1.9 round — flagging as open below rather than resolving unilaterally.

## Artifacts
| Artifact | Status | Canonical location |
|---|---|---|
| Website | Live | https://phtc.org.nz ; private repo `phtc-site` |
| Founding narrative | Live draft, "Guiding Principles" | `narrative.md` (here) + on the site (site copy stale, see above) |
| Constitution | Draft v1.9, pending legal review | `constitution.md` (here) |
| Bylaws | Draft v1.2 | `bylaws.md` (here) |
| Change log (v1.6→v1.9 / v1.0→v1.2) | Reference doc, not mirrored here | Desktop Claude Code workspace (`PHTC_ChangeLog_v1.9.docx`) |

## Open questions / in flight
- Volunteer management and contact capture: needed, not yet designed. The "How can I help" menu item is interim and points to the Get-in-touch section.
- Formation path (transform CMBC vs fresh incorporate) undecided, pending due diligence and the 27 July financials review.
- **Naming convention conflict:** narrative draft now titles the org "... Incorporated" while it isn't incorporated yet. Needs a decision: hold the line on "in formation" copy, or update the convention.
- **Site sync:** live website narrative still shows the old "Statement of Principles" title and "Riding Public Representative" term. Needs updating to match `narrative.md` v1.9-round text.
- Open flags for Simon Price (legal review), carried from the change log:
  - Constitution 8.3 — two-thirds conflict-SGM threshold (s67 modification of s64(3)): confirm the Incorporated Societies Regulations 2023 impose no condition on this; if they do, revert to 50%.
  - Constitution clause 12 (Schedule 2 dispute procedures) — the adoption is a restatement, not a verbatim copy; diff against Schedule 2 of the Act to confirm no paraphrase reads as inconsistent.
  - Constitution 5.7 — written resolutions pass at 75% under s89; consider excluding constitutional amendments from that route so a 75% email round can't carry an amendment without a meeting.
  - Constitution 8.1 — duties are cited as ss54–61 of the Act; confirm whether that whole-subpart citation (vs. the precise 54–60 range) is the preferred form.
  - Word Compare v1.6→v1.9 has not been run yet; do this as a backstop before Simon reviews.
- **Stale cross-reference found while mirroring text here:** `constitution.md` Schedule 1 still says "per clause 18.4" — a leftover from before the DOT-section renumbering. Should read clause 17.4 (Transitional Provisions is now section 17, not 18). Not fixed here since it's a live legal draft; flagging for the desktop session to correct at source.

## Changelog
- 2026-07-06 — Claude Code: created this repo; seeded CONTEXT.md and narrative.md; constitution and bylaws as placeholders.
- 2026-07-06 — browser Claude: corrected formation to two-path (transform CMBC OR fresh incorporate); added LMTBC holding-vessel mechanism and 16 July SGM. Flagged that prior text presented transformation as settled.
- 2026-07-07 — Claude Code (desktop): completed the v1.9 drafting round. Constitution v1.6→v1.9 (Protected Decisions clause 14.1, Riding Public Representative renamed Public Representative, self-nomination-by-condition-report for stewards, AGM window tied to statutory balance-date rule, and more). Bylaws v1.0→v1.2 in step (single Zone Steward, org seat removed, donations clause, governance-role disclosure). Narrative retitled "Guiding Principles," terminology synced. Delivered as `PHTC_Constitution_v1.9_DRAFT.docx`, `PHTC_Bylaws_v1.2_DRAFT.docx`, `phtc_narrative.html`, `PHTC_ChangeLog_v1.9.docx`.
- 2026-07-07 — browser/phone Claude: mirrored the v1.9-round text into `constitution.md`, `bylaws.md`, and `narrative.md` in this repo so all three workspaces read from the same words; carried the Simon Price legal-review flags and the naming/site-sync issues into this file.
