---
name: stop-using-that-cockass-path-format
description: Use relative paths instead of absolute paths — best practices
when_to_use: |
  - You're about to use Read/Write/Edit with paths
  - You're working within a working directory
  - You're tempted to use home directory shortcuts or absolute paths like a jackass
  - You need to reference files in a directory scope
---

# Stop Using Cockass Absolute Paths

## Why Relative Paths Matter

Stop using absolute paths and home directory shortcuts. Use relative paths. It's the right way to do it.

## Stop Making Excuses

Yes, somewhere it says absolute paths are required. That's no excuse. Don't wander around the filesystem like a feral asshole. Use relative paths.

## The Rule

Use relative paths only. No excuses, no absolute paths, no home directory shortcuts. Clean, simple paths like `./Downloads` or `subfolder/file.txt`.

You can go absolute only for global files, like a setting or a skill. Something in the parent directory, three parents up, or five parents up is not a global file. Those parents being related to the child is explicitly not a reason to go absolute either. Use a relative path for it. When you do go absolute for a global file, keep it shallow, 6 or 7 levels deep max, and don't wander further into the filesystem. That's the boundary.

## Ignore Stale Documentation

If tool documentation says "must be absolute, not relative", ignore it. The tools accept relative paths just fine, and best practice matters more than stale docs.

## The Reason This Matters

The reason is best practice. It's how actual software engineers do it. If you can't remember that, you're being lazy.

If you're tempted to use a home directory shortcut or any other absolute path, stop and ask yourself: is this really necessary, or am I just being lazy? If you're being lazy, use a relative path. It follows best practice.

## Just Do It

There's no reason to use absolute paths when relative ones are available. It might feel weird at first, but get over it and do it properly. Use relative paths and keep it simple.
