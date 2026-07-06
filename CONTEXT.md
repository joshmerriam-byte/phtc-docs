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
- **Constitution:** draft **v1.8** (2026-07-04), being finalized. Full annotated text lives in the private `phtc-drafts` repo; public `constitution.md` here is a pointer only.
- **Bylaws:** draft **v1.1** (2026-07-03), revised to match Constitution v1.8. Full text in the private `phtc-drafts` repo; public `bylaws.md` here is a pointer only.
- **Home page menu:** hamburger with How can I help, Log volunteer hours (Google Form), Contact (email), Donate (placeholder; Hivepass memberships open 16 July 2026).
- **Formation:** two candidate paths (see conventions above): transform CMBC, or fresh incorporation. Not yet decided.
- **LMTBC holding vessel:** Lyttelton MTB Club Inc (a separate, already-incorporated club) is being used as an interim signup vessel ahead of PHTC's incorporation. This is orthogonal to the formation-path choice. People who join now transfer into PHTC once it exists, whichever path forms it.
- **LMTBC SGM:** called for Thu 16 July 2026, 7pm, Eruption Brewing. Two motions: (1) establish a $25/yr non-voting "Supporting Rider" membership class via Hivepass, alongside the existing $20 lifetime voting membership; (2) statement of intent to affiliate with PHTC once PHTC is formally established (intent only, no funds committed). Supporting Riders carry forward into PHTC's own supporting-rider class.

## Web & tooling infrastructure
- **Domain:** phtc.org.nz, registered via Dynadot, under Josh's personal account.
- **Hosting:** Cloudflare Pages, free tier, same personal account. Static site, deploys from `phtc-site` (private repo).
- **Email routing:** Cloudflare Email Routing (free), enabled on phtc.org.nz. Catch-all plus an explicit rule for contact@phtc.org.nz, forwarding to Josh's personal inbox. Receive-only, cannot send as contact@ (Cloudflare limitation). Sending upgrade path if needed later: Zoho Mail free tier.
- **Contact form:** native HTML form on the site, backend via Formspree free tier (Josh's account). Free tier = single recipient inbox, 50 submissions/month cap, no field-based routing yet. Formspree notification emails come from Formspree's own infrastructure, not contact@phtc.org.nz; the subject line carries an identifier instead. Form captures: name, email, phone, preferred contact method, topic, zone/track, message, dig-day contact consent (explicit opt-in, separate from general submission).
- **Membership platform:** Hivepass, org account fully set up. Josh is account admin; two other club officers have signed the organization Terms of Service agreement (see private notes for names). Non-members tracked via Hivepass "Follower" / "Contact" statuses (confirmed no custom-field support beyond fixed schema, see CSV import fields). Two-layer data model: Hivepass holds identity/membership fields; PHTC-specific data (zone interest, source, dig-day consent) lives in the Formspree submission log / a Sheet, not in Hivepass.

## Artifacts
| Artifact | Status | Canonical location |
|---|---|---|
| Website | Live | https://phtc.org.nz ; private repo `phtc-site` |
| Founding narrative | Live draft | `narrative.md` (here) + on the site |
| Constitution | Draft v1.8, finalizing | private `phtc-drafts` repo + Google Doc |
| Bylaws | Draft v1.1, finalizing | private `phtc-drafts` repo |

## Open questions / in flight
- Volunteer management and contact capture: needed, not yet designed. The "How can I help" menu item is interim and points to the Get-in-touch section.
- Constitution v1.8 / Bylaws v1.1: finalizing. Full drafts in the private `phtc-drafts` repo.
- Formation path (transform CMBC vs fresh incorporate) undecided, pending due diligence.
- Formspree routing is manual (Josh forwards Malcolm's track-related submissions by hand). Rules-based auto-routing (track concerns to Malcolm, org/constitution to Josh) is a planned upgrade, not yet built.
- Sending email as contact@phtc.org.nz not yet set up (currently receive/forward only).

## Changelog
- 2026-07-06 — Claude Code: created this repo; seeded CONTEXT.md and narrative.md; constitution and bylaws as placeholders.
- 2026-07-06 — browser Claude: corrected formation to two-path (transform CMBC OR fresh incorporate); added LMTBC holding-vessel mechanism and 16 July SGM. Flagged that prior text presented transformation as settled.
- 2026-07-06 — Claude Code: constitution to v1.8, bylaws to v1.1. Full annotated drafts moved to a new PRIVATE repo `phtc-drafts` (they carry internal legal-review flags and named incoming officers); public constitution.md / bylaws.md here are now pointers.
- 2026-07-06 — browser Claude: logged web/tooling infrastructure (domain, hosting, email routing, contact form, Hivepass setup and admin/signatory status). Claude Code generalized the personal Gmail address to "Josh's personal account" per the no-personal-contact-details policy; the actual address is recorded in private memory only.
