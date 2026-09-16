# Circulating the constitution for committee approval

**For Tanya.** Constitution v1.22 and Bylaws v1.5, commit `a114fca`, 16 September 2026.

What to publish, what to send, how members record an approval, and what to do when someone objects.

---

## What is being circulated

Two governing documents and two explainers. The documents are what gets approved; the explainers exist so people can approve them without reading 400 clauses cold.

- **Constitution v1.22** and **Bylaws v1.5** — the text itself
- **Reading guide** — the ten changes that matter most, and the charitable purposes to check
- **CMBC comparison** — what the law required us to change, and what we chose to change

Label everything **"for committee approval — v1.22"**. This round of approval is what makes the documents final, so don't call them final beforehand.

---

## Document fingerprints

Each document has a fingerprint: change a single character and it changes completely. Publish these alongside the files so anyone can confirm the copy they are reading is the copy being approved.

| Document | Fingerprint | Size |
|---|---|---|
| Constitution v1.22 | `5617b6da2846` | 46,298 bytes |
| Bylaws v1.5 | `1e30f199c183` | 30,616 bytes |
| Source commit | `a114fca` | 16 Sep 2026 |

Most people will never check these, and that is fine. They exist so that if two copies ever disagree, there is a fast way to tell which one is right.

> **What this proves.** A fingerprint reliably catches accidental differences — an old copy, a mangled conversion, a half-finished download. It is not protection against someone who controls the website, since they could change the file and the fingerprint together. That is the right level of assurance for this job, and worth describing accurately rather than overselling.

---

## The process, in order

### 1. Publish, before anyone is notified

The documents go live on phtc.org.nz first, so that every link in the notice works the moment it lands. Nothing is worse than a governance email pointing at a 404.

Check the page yourself on a phone before sending. Most committee members will open it on one.

### 2. Send the notice to every committee member individually

Not as a group thread. Each person needs to reply with their own position, and group threads produce three replies and eight silences.

Use the text below. Set a deadline at least **ten clear days** out — long enough to read properly, short enough to stay urgent — and put the actual date in, never "two weeks".

### 3. Keep a register as replies arrive

One row per member, recording:

- Name
- Date replied
- **Which version** they approved — record `v1.22 / 5617b6da2846`
- Approve, approve with comments, or object
- Their comments verbatim

Recording the version matters more than it sounds. If the text changes after someone approves, their approval no longer covers the current document and they need to be asked again.

### 4. Chase the silent ones at the halfway mark

A single short reminder to anyone who has not replied, roughly five days in. **Silence is not approval and must not be recorded as approval.**

### 5. Close the round and report

After the deadline, send the committee a summary: how many approved, what comments came in, and what is proposed in response to each. Anything that changes the text produces a new version and a new fingerprint, and the people who already approved need to see what changed.

---

## The notice to send

Fill in the bracketed parts. Keep it short — the explainers do the heavy lifting.

> **Subject:** PHTC constitution v1.22: your approval needed by [date]
>
> Hi [name],
>
> The PHTC constitution and bylaws are ready for committee approval. I need a yes or no from you by **[date]**.
>
> Everything is here: **[link]**
>
> If you read nothing else, read these two things:
>
> - The **reading guide**, which covers the ten changes that matter most. It takes about ten minutes.
> - **Clause 3.2, the charitable purposes.** These define what the organisation is allowed to do and what Charities Services will register us against. They are much harder to change later, so this is the part we most need checked.
>
> There is also a comparison against the current CMBC constitution, setting out what the Incorporated Societies Act 2022 forced us to change and what we chose to change. The chosen ones are the ones worth arguing about.
>
> Reply to this email with one of:
>
> - **Approve**
> - **Approve with comments** — and the comments
> - **Object** — and what would need to change
>
> Quote the clause number for anything specific, so comments can be tracked against the text.
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

The first twelve characters of the result should read `5617b6da2846`. If they do not, they have the wrong file or an incomplete download — send them the link again.

---

## When someone objects

An objection is not a problem to be managed, it is the process working. Three things to get right:

**Acknowledge within a day**, even if the answer takes longer. Silence after an objection reads as dismissal.

**Separate the two kinds.** Some changes came from CCC rangers and we will generally follow CCC — those are explainable but not very negotiable. Others came from our own drafting and are genuinely open. Say which is which rather than defending everything equally.

**If the text changes, re-circulate.** A new version gets a new fingerprint, and anyone who approved the previous version is told what changed and asked to confirm. Approval attaches to a specific text, not to the idea of the document.

---

*Port Hills Trails Collective — in formation. Circulation brief for Constitution v1.22 and Bylaws v1.5, commit `a114fca`.*
