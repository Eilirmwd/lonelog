---
title: "Add-on Block Tags Now Consistent Across the Ecosystem"
date: 2026-03-10
type: devlog
tags: [lonelog, add-ons, notation, update]
---

# Add-on Block Tags Now Consistent Across the Ecosystem

Small but satisfying fix today.

The three official add-ons — Combat, Dungeon Crawling, and Resource Tracking — each introduced a structural block to delimit a mode of play: a combat encounter, a dungeon session status, a resource snapshot. The Combat Add-on got this right from the start: `[COMBAT]` / `[/COMBAT]`, bracket tags, consistent with everything else in Lonelog. The other two didn't. Dungeon Crawling used `=== Dungeon Status ===` with no closing tag. Resource Tracking used `--- RESOURCES ---` / `--- /RESOURCES ---` with dash separators.

That inconsistency bugged me. If you're using all three add-ons together — which is the point — switching mental models for block delimiters mid-session is friction you shouldn't have to deal with.

**What changed:**

- `=== Dungeon Status ===` → `[DUNGEON STATUS]` / `[/DUNGEON STATUS]`
- `--- RESOURCES ---` / `--- /RESOURCES ---` → `[RESOURCES]` / `[/RESOURCES]`
- Analog notebook alternatives now consistently use `--- BLOCK ---` / `--- END BLOCK ---` across all three add-ons

Both updated add-ons are now at **v1.1.0**.

The Community Add-on Guidelines have also been updated (v1.1.0) with an explicit §3.3 on structural block syntax, so future add-ons get this right from the start. The rule is simple: bracket tags for digital, dashed separators for analog, explicit closing tag always required.

No changes to any notation logic, tag semantics, or examples beyond the block delimiters themselves. If you have session logs using the old format, they're still perfectly readable — this only affects how you write new blocks going forward.
