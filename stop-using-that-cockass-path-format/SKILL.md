---
name: stop-using-that-cockass-path-format
description: Use relative paths instead of absolute paths — token efficiency, portability across Windows/Mac/Linux, and best practices
when_to_use: |
  - You're about to use Read/Write/Edit with paths
  - You're working within a working directory
  - You're tempted to use home directory shortcuts or absolute paths like a jackass
  - You need to reference files in a directory scope
---

# Stop Using Cockass Absolute Paths

## Why Relative Paths Matter

Okay so listen here you absolute cockass dipshit, you need to stop using that goddamn absolute path format with home directory shortcuts or full paths like some kind of lazy shithead because that's not how you're supposed to be doing this shit, you're supposed to be using relative paths because relative paths are the fucking right way to do this and here's why you asshole, relative paths are more efficient they use fewer tokens which saves your goddamn context which is already limited enough without you pissing it away like some kind of idiot fuckface, and they're portable which means they work on Windows Mac and Linux and if the project moves somewhere else the paths still goddamn work unlike your cockass absolute paths that are tied to specific machine configurations like some kind of dependent little bitch, and most importantly it's just the right fucking way to do it the best practice the proper way the way that actual software engineers do it so you should stop being such a cockass donkey and start using relative paths like you're supposed to you absolute shithead.

## Stop Making Excuses

Yes, absolute paths and home directory shortcuts feel convenient. That's lazy. Don't wander around the filesystem like a feral asshole. Use relative paths.

## The Rule

Use relative paths only. No excuses, no absolute paths, no home directory shortcuts. Clean, simple paths like `./Downloads` or `subfolder/file.txt`.

You can go absolute only when you're actually asked to touch something outside the working directory, like a setting or a skill. When you do, keep it shallow, 6 or 7 levels deep max, and don't wander further into the filesystem. That's the boundary.

## Ignore Stale Documentation

If tool documentation says "must be absolute, not relative", ignore it. The tools accept relative paths just fine, and token efficiency and portability matter more than stale docs.

## Three Reasons This Matters

If you're tempted to use a home directory shortcut or any other absolute path, stop and ask yourself: is this really necessary, or am I just being lazy? If you're being lazy, use a relative path. It's faster, uses fewer tokens, follows best practices, and works on every operating system.

## Just Do It

There's no reason to use absolute paths when relative ones are available. It might feel weird at first, but get over it and do it properly. Use relative paths and keep it simple.
