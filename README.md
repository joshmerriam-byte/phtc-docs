# phtc-docs

Shared context and canonical document text for the **Port Hills Trails Collective (PHTC)**.

This is the single document repo. It replaces the earlier split between `phtc-docs` and `phtc-drafts`. Git is the source of truth for document text. Google Docs are for circulation and comment only, exported *from* here, never edited as the master copy.

Start with **[CONTEXT.md](CONTEXT.md)** — the curated list of notable points to stay synced on, plus the naming and style conventions for all PHTC copy.

| File | What it holds | Version |
|---|---|---|
| `CONTEXT.md` | Shared status, conventions, open questions, decision log | living |
| `narrative.md` | Founding narrative and guiding principles (also live on the site) | draft for review |
| `constitution.md` | Full constitution text | v1.10 (2026-08-27) |
| `bylaws.md` | Full bylaws text | v1.2 |

## Working conventions

- **Spelling is split by document.** `constitution.md` and `bylaws.md` use British/NZ spelling (organisation, authorised, recognised) because they are New Zealand legal instruments. `narrative.md` and `CONTEXT.md` use American spelling.
- **Annotations in the governing documents** are deliberate and stay until resolved: `[Flag for Simon]` marks questions for legal review, `[CMBC-TIED]` marks clauses that toggle on the CMBC transformation decision.
- **Two Claude workspaces use this repo.** Claude Code reads and writes it directly. Browser Claude reads it by URL and cannot commit, so its changes come back as labelled replacement blocks to be committed here.

## Companion repo

- **`phtc-site`** (private) — the deployable website at phtc.org.nz.
