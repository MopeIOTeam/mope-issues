# Contributing Guidelines

Thank you for helping improve Mope.io! Because the game is closed-source,
contributing here means writing **clear, actionable issue reports**. Please
read these rules carefully — they exist so developers can actually find, fix,
and close what you report.

> GitHub automatically links to this file when you open a new issue.

---

## 1. One Issue = One Problem

This is the single most important rule.

Open a **separate** issue for each bug, visual problem, AI issue, balance
concern, or suggestion. Do **not** bundle unrelated problems together.

A report like "here are 90 things that are broken" is impossible to triage,
assign, or close. **Mega-list issues will be closed** and you will be asked to
resubmit them as individual reports.

### Bad

> **Title:** visual feedback/bugs and a few gameplay bugs
>
> - shrimp doesn't boost when hurt
> - desert chipmunk has no cheeks asset
> - pig's fart grows way too big
> - seahorse's ability seems broken
> - jellyfish can stun all animals
> - *(…80 more unrelated items)*

This was [an actual issue in this repo](#23). Don't do this.

### Good

> **Title:** [Bug] Jellyfish stun affects all tiers including Black Dragon
>
> Jellyfish's stun has no tier cap. It can stun any animal up to and
> including Black Dragon. Expected: limited to tier 13 or below.

---

## When Multiple Bugs ARE Related

If several bugs clearly affect the **same animal AND the same system**
(ability, animation, asset set), they **can** go in one issue.

### Acceptable as one issue

> **Title:** [Visual] Peacock — multiple issues during Hypnotize ability
>
> When using the Hypnotize ability:
> - Peacock's body asset disappears entirely
> - Wings are stretched too far from the body
>
> Both occur during the same ability animation and likely share a root cause.

### Also acceptable

> **Title:** [Bug] Fennec Fox — same-species stun + missing passive animation
>
> - Fennec Foxes can stun other Fennec Foxes (same-species stun should
>   be blocked)
> - Fennec Fox still has no passive ear animation
>
> Both relate to the Fennec Fox's core behavior.

### NOT acceptable

> Fennec Fox has no ear animation, also Pelican is too fast, also Yeti
> shoots 6 snowballs.

These are three completely unrelated animals. File them separately.

**Rule of thumb:** same animal + same system = okay to group.
Different animals or different systems = separate issues.

---

## When a Bug Is Systemic

Some bugs affect many animals because of shared underlying logic — for
example, "all same-species abilities can stun each other" or "all flying birds
are translucent to their own player."

In these cases, file **one** issue describing the **systemic pattern**, list
the affected animals as examples, and title it after the shared mechanic
rather than a single animal:

> **Title:** [Bug] Same-species ability stun is not blocked for multiple animals
>
> Affected: Jellyfish, Stingray, Pufferfish, Wolf, Fennec Fox.
> All of these can stun members of their own species with their ability.
> Expected: same-species stun should be blocked.

This is acceptable because the root cause is clearly one shared system, not
five unrelated bugs.

---

## 2. Search Before Posting

Before opening a new issue:

1. Search [open issues](../../issues)
2. Search [closed issues](../../issues?q=is%3Aissue+is%3Aclosed)
3. If the same problem exists, add new evidence or a 👍 there instead

Duplicates will be closed and linked to the original.

---

## 3. Write Clear Titles

Use this format:

```
[Type] Animal or feature — short description
```

### Types

| Type | Use when… |
|---|---|
| `Bug` | Something doesn't work as intended |
| `Visual` | Wrong asset, missing animation, stretched/squished art, transparency |
| `AI` | NPC / bot behavior is wrong |
| `Balance` | Works as coded but feels too strong, weak, fast, or slow |
| `Regression` | Used to work, now broken after an update |
| `Suggestion` | New idea or design change |

### Examples

- ✅ `[Bug] Toucan cannot throw food after flying from under a tree`
- ✅ `[Visual] Fennec Fox has no passive ear animation`
- ✅ `[AI] Fish AI are treated as real players and barely give XP`
- ✅ `[Regression] Snow Leopard can no longer climb rocks`
- ❌ `bugs`
- ❌ `lots of issues`
- ❌ `BUGGGG PLZ FIX`

---

## 4. Include Enough Detail

A useful report contains:

| Field | Example |
|---|---|
| **Animal / feature** | Toucan |
| **Context** | Desert biome, under a tree, on land |
| **Steps to reproduce** | 1. Pick Toucan → 2. Fly under a tree → 3. Grab food → 4. Leave tree → 5. Try to throw |
| **Expected result** | Toucan throws the food normally |
| **Actual result** | Throw doesn't happen; food stays grabbed |
| **Frequency** | Always / Often / Sometimes / Rarely / Once |
| **Game version or date** | Noticed after the May 2025 update *(if known)* |
| **Browser / device** | Chrome, desktop *(if relevant)* |
| **Evidence** | Screenshot, GIF, or video link |

> **Game version:** If you know which update introduced or changed the
> behavior, mention it. This helps narrow down regressions enormously. Even
> a rough date ("started after the last patch") is useful.

---

## 5. Bugs vs. Feedback

Use the correct template:

- **Bug Report** — something does not work as intended (broken ability,
  wrong asset, AI misbehavior, collision issue)
- **Feature / Balance Request** — something works but feels wrong, or you
  want something new

Do not mix categories in one issue.

---

## 6. Exploits and Sensitive Issues

Do **not** post detailed exploit or cheat instructions publicly. If the issue
can be abused, report it privately via the
[Discord server](https://discord.com/invite/nQAVB9c) instead of filing a
public issue.

---

## 7. Account, Payment, and Ban Issues

This repository is **not** for account support. For account, payment, or ban
issues, submit a ticket at:

🔗 **https://support.vexxusarts.com/submit-ticket/2-mopeio**

Issues filed here for account support will be closed immediately.

---

## 8. Language

Issues should be written in **English**. If English is not your first
language, do your best — we appreciate the effort. You may include a
description in your native language *in addition to* an English summary if
that helps communicate the problem more clearly.

---

## What Will Get Your Issue Closed

| Reason | Policy |
|---|---|
| Mega-list of unrelated bugs | Closed; resubmit individually |
| Duplicate | Closed with link to original |
| No useful information / too vague | Labeled `needs-info`; closed after 14 days if no response |
| Not a bug (intentional behavior) | Closed with explanation |
| Account / ban / payment support | Closed; use [Support Tickets](https://support.vexxusarts.com/submit-ticket/2-mopeio) |
| Hostile or disrespectful tone | Closed; repeated offenses may result in a repo ban |

---

## Moderation

Maintainers are developers assigned to Mope.io by 3AM Experiences LLC. They
are responsible for labeling, confirming, prioritizing, and closing issues.
Only maintainers create umbrella or tracking issues.

If you disagree with a closure, reply politely on the closed issue with new
evidence. Do not open a new issue to argue about a closed one.

---

## Summary Cheat Sheet

| ✅ Do | ❌ Don't |
|---|---|
| One bug per issue | Dump 50 bugs in one issue |
| Search for duplicates first | Assume nobody reported it |
| Include the animal name in the title | Use vague titles |
| Describe expected vs. actual behavior | Just say "it's broken" |
| Group related bugs for the **same animal + system** | Group bugs just because you found them at the same time |
| Include reproduction steps | Assume we know what you mean |
| Attach screenshots or video | Leave a text-only report for visual bugs |
| Use [Support Tickets](https://support.vexxusarts.com/submit-ticket/2-mopeio) for account issues | File account/ban issues here |
| Report exploits privately on [Discord](https://discord.com/invite/nQAVB9c) | Post exploit details publicly |
| Mention the game version or date | Omit when the bug started |

Thank you for helping make Mope.io better!
