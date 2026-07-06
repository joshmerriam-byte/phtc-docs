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
_As of 2026-07-06:_
- **Website:** live at https://phtc.org.nz. Cloudflare Pages, auto-deploys on push to the private `phtc-site` repo. Pages: home + founding narrative.
- **Founding narrative:** live on the site, marked "Draft for review". Canonical text mirrored in `narrative.md` (this repo).
- **Constitution:** draft **v1.7** being finalized (Google Doc, comments enabled, linked from the website). Text not yet mirrored here.
- **Bylaws:** not yet drafted.
- **Home page menu:** hamburger with How can I help, Log volunteer hours (Google Form), Contact (email), Donate (placeholder; Hivepass memberships open 16 July 2026).
- **Formation:** two candidate paths (see conventions above): transform CMBC, or fresh incorporation. Not yet decided.
- **LMTBC holding vessel:** Lyttelton MTB Club Inc (a separate, already-incorporated club) is being used as an interim signup vessel ahead of PHTC's incorporation. This is orthogonal to the formation-path choice. People who join now transfer into PHTC once it exists, whichever path forms it.
- **LMTBC SGM:** called for Thu 16 July 2026, 7pm, Eruption Brewing. Two motions: (1) establish a $25/yr non-voting "Supporting Rider" membership class via Hivepass, alongside the existing $20 lifetime voting membership; (2) statement of intent to affiliate with PHTC once PHTC is formally established (intent only, no funds committed). Supporting Riders carry forward into PHTC's own supporting-rider class.

## Artifacts
| Artifact | Status | Canonical location |
|---|---|---|
| Website | Live | https://phtc.org.nz ; private repo `phtc-site` |
| Founding narrative | Live draft | `narrative.md` (here) + on the site |
| Constitution | Draft v1.7, finalizing | Google Doc (linked from the website) |
| Bylaws | Not started | — |

## Open questions / in flight
- Volunteer management and contact capture: needed, not yet designed. The "How can I help" menu item is interim and points to the Get-in-touch section.
- Constitution v1.7: finalizing. Once stable, paste the text into `constitution.md` so both Claudes work from the same words.
- Formation path (transform CMBC vs fresh incorporate) undecided, pending due diligence.

## Changelog
- 2026-07-06 — Claude Code: created this repo; seeded CONTEXT.md and narrative.md; constitution and bylaws as placeholders.
- 2026-07-06 — browser Claude: corrected formation to two-path (transform CMBC OR fresh incorporate); added LMTBC holding-vessel mechanism and 16 July SGM. Flagged that prior text presented transformation as settled.
