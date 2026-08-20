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
_As of 2026-07-16:_
- **Website:** live at https://phtc.org.nz. Cloudflare Pages, auto-deploys on push to the private `phtc-site` repo. Pages: home + founding narrative.
- **Founding narrative:** live on the site, marked "Draft for review". Canonical text mirrored in `narrative.md` (this repo).
- **Constitution:** draft **v1.9** (2026-07-07), being finalized. Full text now lives in this repo (`constitution.md`), not a pointer. `phtc-drafts` is retired; see Repo structure below.
- **Bylaws:** draft **v1.2**, revised to match Constitution v1.9. Full text in this repo (`bylaws.md`), not a pointer.
- **Repo structure:** `phtc-docs` is now the single document repo (context, narrative, constitution, bylaws). The former private `phtc-drafts` repo is retired; delete once confirmed nothing was lost. Git is the source of truth for document text. Google Docs are for circulation and comment only, exported from here, never edited as the master copy.
- **Dig Otautahi (DOT):** as of v1.9, no DOT-specific provisions (preferred-partner language, named conflict-of-interest clauses) exist anywhere in the constitution, bylaws, or narrative. Any such text either never made it out of an earlier draft or lives only in a version not yet recovered. If it resurfaces, it needs the same review this change list gave everything else, not a silent re-add.
- **No-surprises commitment:** added to constitution 3.5 and the narrative's closing commitment: Society-organized trail work is agreed with the land manager before it starts and delivered as described. This "No Surprises" policy formalizes the same understanding the Vic Park committee and Dig Otautahi already operate under.
- **CMBC AGM:** the meeting where CMBC members vote on the transformation into PHTC is set for **7 September 2026**.
- **Amendment threshold (transformation vote):** CMBC's own constitution requires a simple majority to approve adopting the new PHTC constitution, pending legal confirmation. This is separate from PHTC's own constitution, which requires a 75% Special Resolution for future amendments (clause 14) once adopted.
- **Home page menu:** hamburger with Get in touch (form + email fallback), Log volunteer hours (Google Form), Contact form (#contact), Donate (live: Hivepass Supporting Rider signup).
- **Hivepass link:** use the dynamic smart-link go.hivepass.app/TxiS (generated from the Hivepass QR feature after uploading a club logo). This opens the Hivepass app for members who have it installed, else falls back to browser. Do NOT use join.hivepass.app/lmtbc (app doesn't claim that domain, always went to browser). Testing established the app only routes via go.hivepass.app / member.hivepass.app; join.* and org-path URLs failed.
- **LMTBC logo:** simple green rounded-square badge (wheel + Port Hills ridgeline + "Lyttelton Mountain Bike Club" wordmark, amber accents), created as a temporary mark to unblock the Hivepass logo upload. Source SVG + 1024px PNG in C:\Claude\lmtbc-logo\ (not committed to a repo).
- **Public contact address:** contact@phtc.org.nz (shown on the site's Get in touch fallback link). Currently forwards to Josh; can be silently repointed to another address or multiple people on the back end without a site change. Replaces the earlier personal-email fallback.
- **Formation:** two candidate paths (see conventions above): transform CMBC, or fresh incorporation. Not yet decided.
- **LMTBC holding vessel:** Lyttelton MTB Club Inc (a separate, already-incorporated club) is being used as an interim signup vessel ahead of PHTC's incorporation. This is orthogonal to the formation-path choice. People who join now transfer into PHTC once it exists, whichever path forms it.
- **LMTBC SGM:** called for Thu 16 July 2026, 7pm, Eruption Brewing. Two motions: (1) establish a $25/yr non-voting "Supporting Rider" membership class via Hivepass, alongside the existing $20 lifetime voting membership; (2) statement of intent to affiliate with PHTC once PHTC is formally established (intent only, no funds committed). Supporting Riders carry forward into PHTC's own supporting-rider class.

## Web & tooling infrastructure
- **Domain:** phtc.org.nz, registered via Dynadot, under Josh's personal account.
- **Hosting:** Cloudflare Pages, free tier, same personal account. Static site, deploys from `phtc-site` (private repo).
- **Email routing:** Cloudflare Email Routing (free), enabled on phtc.org.nz. Catch-all plus an explicit rule for contact@phtc.org.nz, forwarding to Josh's personal inbox. This is the address now shown publicly on the site (see Current status); the forward target can change without touching the site. Receive-only, cannot send as contact@ (Cloudflare limitation). Sending upgrade path if needed later: Zoho Mail free tier.
- **Contact form:** native HTML form on the site, backend via Formspree free tier (Josh's account). Free tier = single recipient inbox, 50 submissions/month cap, no field-based routing yet. Formspree notification emails come from Formspree's own infrastructure, not contact@phtc.org.nz; the subject line carries an identifier instead. Form captures: name, email, phone, preferred contact method, topic, zone/track, message, dig-day contact consent (explicit opt-in, separate from general submission).
- **Membership platform:** Hivepass, org account fully set up. Josh is account admin; two other club officers have signed the organization Terms of Service agreement (see private notes for names). Non-members tracked via Hivepass "Follower" / "Contact" statuses (confirmed no custom-field support beyond fixed schema, see CSV import fields). Two-layer data model: Hivepass holds identity/membership fields; PHTC-specific data (zone interest, source, dig-day consent) lives in the Formspree submission log / a Sheet, not in Hivepass.

## Artifacts
| Artifact | Status | Canonical location |
|---|---|---|
| Website | Live | https://phtc.org.nz ; private repo `phtc-site` |
| Founding narrative | Live draft | `narrative.md` (here) + on the site |
| Constitution | Draft v1.9, finalizing | `constitution.md` (here) + Google Doc for circulation |
| Bylaws | Draft v1.2, finalizing | `bylaws.md` (here) |

## Open questions / in flight
- Volunteer management and contact capture: needed, not yet designed. The "How can I help" menu item is interim and points to the Get-in-touch section.
- Constitution v1.9 / Bylaws v1.2: finalizing.
- Formation path (transform CMBC vs fresh incorporate) undecided, pending due diligence. CMBC AGM to vote on the transform path set for 7 September 2026.
- Formspree routing is manual (Josh forwards Malcolm's track-related submissions by hand). Rules-based auto-routing (track concerns to Malcolm, org/constitution to Josh) is a planned upgrade, not yet built.
- Sending email as contact@phtc.org.nz not yet set up (currently receive/forward only).
- Purpose clauses (constitution 3.2): softened language for "voice for riders and stewards, not sole representative" is drafted but not yet placed. Needs a decision on whether it becomes a new purpose clause 3.2(f) or replaces existing wording, since no current clause actually overclaims construction or sole-representative status.
- Schedule 1 (Founding Members) is still an empty placeholder. The Vic Park / Gravity Canterbury / Zone 15 steward-seat split described in an earlier change list can't be applied until Schedule 1 has real entries to split.
- Schedule 2 (land manager and community contacts) does not exist in the current constitution. Adding named individuals (e.g., CCC rangers, community supporters) needs their confirmation before anything is committed to a public repo, and needs the schedule to exist first.

## Changelog
- 2026-07-06 — Claude Code: created this repo; seeded CONTEXT.md and narrative.md; constitution and bylaws as placeholders.
- 2026-07-06 — browser Claude: corrected formation to two-path (transform CMBC OR fresh incorporate); added LMTBC holding-vessel mechanism and 16 July SGM. Flagged that prior text presented transformation as settled.
- 2026-07-06 — Claude Code: constitution to v1.8, bylaws to v1.1. Full annotated drafts moved to a new PRIVATE repo `phtc-drafts` (they carry internal legal-review flags and named incoming officers); public constitution.md / bylaws.md here are now pointers.
- 2026-07-06 — browser Claude: logged web/tooling infrastructure (domain, hosting, email routing, contact form, Hivepass setup and admin/signatory status). Claude Code generalized the personal Gmail address to "Josh's personal account" per the no-personal-contact-details policy; the actual address is recorded in private memory only.
- 2026-07-06 — Claude Code: narrative.md synced with the live site; added "guiding" to principles in the title and transition line.
- 2026-07-06 — Claude Code: site's email fallback switched from Josh's personal address to contact@phtc.org.nz (forwards to Josh, repointable on the back end without a site change).
- 2026-07-16 — Claude Code: activated the Donate link (menu) to the live Hivepass membership signup, join.hivepass.app/lmtbc. All site placeholders now wired.
- 2026-07-16 — Claude Code: made a temporary LMTBC logo, uploaded to Hivepass to unblock the QR feature; swapped Donate to the resulting dynamic smart-link go.hivepass.app/TxiS (opens the app if installed, else browser). Removed the deep-link test scaffolding.
- 2026-07-16 — Claude Code: consolidated `phtc-drafts` into `phtc-docs`. Brought in full constitution v1.9 and bylaws v1.2 (recovered from a Google Docs export, since the versions had drifted out of git via an earlier browser-Claude session that had no way to commit). Applied a reviewed change list: added the no-surprises clause to constitution 3.5 and the narrative, added an explicit land-manager-decides clause (5.1), confirmed the franchise-reservation and uniform-steward-lapse items were already resolved in v1.9, narrowed narrative overclaims from "the whole network" to "riders and stewards," and updated Principle 01. Dropped the DOT-removal item as a no-op (no DOT-specific text found anywhere). Purpose-clause softening, Schedule 1 Vic Park split, and Schedule 2 names remain open, see Open questions.
