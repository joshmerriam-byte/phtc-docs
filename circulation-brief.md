# Circulating the constitution for committee approval

**For Tanya.** Constitution v1.23 and Bylaws v1.6, commit `debc018`, 16 September 2026.

What to publish, what to send, how members record an approval, and what to do when someone objects.

---

## What is being circulated

Two governing documents and two explainers. The documents are what gets approved; the explainers exist so people can approve them without reading 400 clauses cold.

Everything is now live on the website. These are the links to use:

| What | Where |
|---|---|
| Reading guide | <https://phtc.org.nz/reading-guide.html> |
| What had to change, and what we chose | <https://phtc.org.nz/constitution-changes.html> |
| Constitution v1.23 (comments enabled) | <https://docs.google.com/document/d/10on11Ete8mjLA2p62M55Iwzc3XWB9xB1/edit> |
| Bylaws draft v1.6 (comments enabled) | <https://docs.google.com/document/d/1JJGRYkx_8FwGmniai0SiImuBXIMjhv8OJm-jBg78v-8/edit> |
| CMBC constitution, 15 Sep 2024 (PDF) | <https://phtc.org.nz/cmbc-constitution-2024-09-15.pdf> |

Both guide pages open with a panel linking all three source documents, so a member who lands on either one can reach everything else without going back to your email.

Label everything **"for committee approval — v1.23"**. This round of approval is what makes the documents final, so don't call them final beforehand.

> **Comments are open on both Google Docs.** That is the easiest way for people to respond, and it puts each comment next to the clause it is about. It also means anyone with the link can comment, since the links are on a public page. Watch for anything odd and tell Josh if you see it.

---

## Document fingerprints

Each document has a fingerprint: change a single character and it changes completely. Publish these alongside the files so anyone can confirm the copy they are reading is the copy being approved.

| Document | Fingerprint | Size |
|---|---|---|
| Constitution v1.23 | `76d0873d7b74` | 46,343 bytes |
| Bylaws v1.6 | `3df1fdbf11e6` | 30,889 bytes |
| Source commit | `debc018` | 16 Sep 2026 |

Most people will never check these, and that is fine. They exist so that if two copies ever disagree, there is a fast way to tell which one is right.

> **What this proves.** A fingerprint reliably catches accidental differences — an old copy, a mangled conversion, a half-finished download. It is not protection against someone who controls the website, since they could change the file and the fingerprint together. That is the right level of assurance for this job, and worth describing accurately rather than overselling.

---

## The process, in order

### 1. Check the pages before anyone is notified

Already published, so this is a check rather than a task. Open both guide pages on a phone, tap through every link in the reference panel at the top, and confirm all three source documents open. Most committee members will read this on a phone.

Confirm the two Google Docs open in **comment** mode for someone who is not you. Easiest test: open one in a private browsing window.

### 2. Send the notice to every committee member individually

Not as a group thread. Each person needs to reply with their own position, and group threads produce three replies and eight silences.

Use the text below. Set a deadline at least **ten clear days** out — long enough to read properly, short enough to stay urgent — and put the actual date in, never "two weeks".

### 3. Keep a register as replies arrive

One row per member, recording:

- Name
- Date replied
- **Which version** they approved — record `v1.23 / 76d0873d7b74`
- Approve, approve with comments, or object
- Their comments verbatim
- Whether they also commented in the Google Doc

That last column matters now that comments are enabled. Responses will arrive in two places, and a doc comment is easy to miss if you are only watching your inbox. Check both docs when you update the register.

Recording the version matters more than it sounds. If the text changes after someone approves, their approval no longer covers the current document and they need to be asked again.

### 4. Chase the silent ones at the halfway mark

A single short reminder to anyone who has not replied, roughly five days in. **Silence is not approval and must not be recorded as approval.**

### 5. Close the round and report

After the deadline, send the committee a summary: how many approved, what comments came in, and what is proposed in response to each. Anything that changes the text produces a new version and a new fingerprint, and the people who already approved need to see what changed.

### 6. Then the members round, which is a separate obligation

This committee round is not the end. The AGM motion on 7 September carried **subject to a new Constitution being agreed and current Members being notified**, and the minutes set the sequence out: vote on the intention, work on the constitution with the Committee, then send the final document to Club Members with the appropriate notice period for feedback.

So once the committee round closes and any resulting changes are made, the same document goes to **all CMBC members** — 62 as at the AGM, not just the six on the committee.

**Notice period:** CMBC's own constitution, clause 8.1, requires 14 days' notice of a motion to amend or replace the constitution. Treat 14 days as the floor and give more if the calendar allows. Josh is confirming with our lawyer whether the Incorporated Societies Act 2022 changes the threshold; that answer may also affect the notice, so check with him before setting the date.

The version and fingerprint discipline above applies to the members round too. If the committee round changes the text, members must receive the new version, and the register should record which version went to whom.

---

## The notice to send

Fill in the bracketed parts. Keep it short — the explainers do the heavy lifting.

> **Subject:** PHTC constitution v1.23: your approval needed by [date]
>
> Hi [name],
>
> The PHTC constitution and bylaws are ready for committee approval. I need a yes or no from you by **[date]**.
>
> **Start here:** https://phtc.org.nz/reading-guide.html
>
> That covers the ten changes that matter most and takes about ten minutes. It links straight through to the constitution, the bylaws and the old CMBC constitution, so you can open any of them as you read.
>
> If you read nothing else, read **clause 3.2, the charitable purposes**. They define what the organisation is allowed to do and what Charities Services will register us against. They are much harder to change later, so this is the part we most need checked.
>
> There is also a comparison against the current CMBC constitution, setting out what the Incorporated Societies Act 2022 forced us to change and what we chose to change: https://phtc.org.nz/constitution-changes.html — the chosen ones are the ones worth arguing about.
>
> **Comments are enabled** on the constitution and the bylaws, so you can comment directly on any clause. That is the easiest way, and it keeps each comment next to the text it is about.
>
> Whether or not you comment there, reply to this email with one of:
>
> - **Approve**
> - **Approve with comments** — and the comments
> - **Object** — and what would need to change
>
> If you comment in the doc rather than here, still reply with your overall position so I can record it.
>
> One item is still with our lawyer and is not holding up your approval: whether CMBC's simple-majority threshold for adopting the new constitution holds under the Incorporated Societies Act 2022.
>
> Thanks,
> Tanya

---

## If someone wants to verify the file

Rare, but if a member asks, this is the answer. It compares their downloaded copy against the published fingerprint.

| Platform | Command |
|---|---|
| Windows | `certutil -hashfile constitution.md SHA256` |
| Mac | `shasum -a 256 constitution.md` |
| Linux | `sha256sum constitution.md` |

The first twelve characters of the result should read `76d0873d7b74`. If they do not, they have the wrong file or an incomplete download — send them the link again.

---

## When someone objects

An objection is not a problem to be managed, it is the process working. Three things to get right:

**Acknowledge within a day**, even if the answer takes longer. Silence after an objection reads as dismissal.

**Separate the two kinds.** Some changes came from CCC rangers and we will generally follow CCC — those are explainable but not very negotiable. Others came from our own drafting and are genuinely open. Say which is which rather than defending everything equally.

**If the text changes, re-circulate.** A new version gets a new fingerprint, and anyone who approved the previous version is told what changed and asked to confirm. Approval attaches to a specific text, not to the idea of the document.

---

*Port Hills Trails Collective — in formation. Circulation brief for Constitution v1.23 and Bylaws v1.6, commit `debc018`.*
