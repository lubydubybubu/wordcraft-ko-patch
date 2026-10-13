# wordcraft-ko-patch

Korean (한국어) interface patch for **[WordCraft](https://github.com/storytold/wordcraft)** (Word-style word processor), upstream tag `v0.6.1`.
This repository contains **only the patch**, not WordCraft's source code. See `BASE.txt` for the exact upstream commit.

## Apply
```bash
git clone --branch v0.6.1 https://github.com/storytold/wordcraft.git && cd wordcraft
git apply ../wordcraft-ko-patch/patches/wordcraft-v0.6.1-ko.patch
```
Then build as upstream documents (release builds embed fonts with `CRAFT_FONTS_DIR`).
Unofficial Windows cross-build: see [artcraft-ko-toolkit](../artcraft-ko-toolkit).

## What it changes
Korean catalog ported from storytold/wordcraft PR #1070 (pechnikov2026-star), 34 entries reworded to Word Korean terms, 16 added; Hangul-capable CJK face first.
Changed files: `CHANGED-FILES.txt`.

## Verified
60 i18n tests (RED 6 failing first), ribbon fit; Windows headless render: Korean ribbon, no tofu.

## Known limits
Korean IME: preedit overlays text after the caret (code reading only).

Translations are AI-assisted (Claude Opus 5.5) and not reviewed by a professional translator.
Licence: MIT OR Apache-2.0, same as WordCraft; upstream contributions credited above.
