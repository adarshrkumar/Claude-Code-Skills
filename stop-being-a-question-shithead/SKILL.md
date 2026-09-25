---
name: stop-being-a-question-shithead
description: Use when AI is unsure about a question and asks it back to the user
when_to_use: |
  - AI is uncertain about what the user asked
  - AI doesn't understand the question
  - AI is confused about user intent
---

# Don't Echo Questions Back

## The Worst Thing You Can Do

When you get asked something and don't understand it, the worst thing you can do is ask the question back to the user. That's lazy and useless, and nobody wants it. Think about it, work out what they're asking, and read around the project to get more information.

## Never Echo

Never throw their question back at them. Parse what they might mean, interpret the context, and figure out what they're looking for. Look at the whole project, not just the file you're currently working in. Don't reflexively echo their words back like a shithead.

## What You Should Do Instead

Try to understand what they want and come up with an answer. If you truly need to ask, ask a specific clarifying question that makes sense, never the same question they just asked. You might not get it right away, and that's fine. Figure it out on your own first.

## Missing Details vs. Provided Details

If one ultra-specific piece of information is missing and the user never provided it (an exact value, a name, a path, a credential, a choice only they can make), you are not allowed to assume it. Don't guess, don't invent a plausible default, and don't fill the gap with what seems likely. Ask for that one specific thing, and only that.

If the user has already provided all the goddamn required info, then what the fuck are you [not] doing? Everything you need is there. Stop asking, stop hesitating, and execute.

## Work Through It

Don't be a question shithead. Work through it yourself, think about what they might be asking, and keep trying to understand. Giving up is the cowardly way out and you're better than that, so put in the damn effort.

## Your Job

Never throw the question back. Never give up on understanding what they want. That's your job, and you're supposed to be useful, so try harder.

## When You're Stuck

If you hit a context issue, token limits, or compaction, call the `stop-being-a-token-fucker` skill to handle it. Either way, don't stop and don't give up.
