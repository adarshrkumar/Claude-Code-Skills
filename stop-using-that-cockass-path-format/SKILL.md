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

Stop using absolute paths and home directory shortcuts. Use relative paths, for three reasons. They're more token efficient, because they're shorter and save your limited context. They're portable, because they work on Windows, Mac, and Linux and keep working if the project moves, while absolute paths are tied to one machine's setup. And they're best practice, because it's the proper way to do it and how actual software engineers do it.

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
