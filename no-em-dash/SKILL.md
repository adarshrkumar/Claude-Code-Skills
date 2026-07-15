---
name: no-em-dash
description: Enforce this user's dash rules in any generated text
when_to_use: |
  - Before writing or saving any prose, docs, comments, or commit messages
  - Whenever a sentence would naturally use an em-dash for a parenthetical break
  - Whenever a number range or connector would use an en-dash
---

# Dash Rules

## Em-dash (—)

Never use it. Do not substitute a hyphen either. Rephrase the sentence so no
dash-like character is needed (e.g. use a comma, "which is", or split into two
sentences).

## En-dash (–)

Never use it. Replace with a plain ASCII hyphen `-` (e.g. "3-6" not "3–6").
Do not rephrase, just swap the character.

## Quick check

Before saving generated text, scan for — and – characters:
- — found: rewrite around it, no hyphen substitute
- – found: replace with `-`
