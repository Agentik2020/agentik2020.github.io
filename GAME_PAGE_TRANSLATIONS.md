# Agentik Studio — Game Detail Description Rules

Use the layout of `cozy-cafe/index.html` for game pages. Game content must be specific to each game.

- Keep an “About the game” heading and the same eight-paragraph structure: introduction, gameplay, unique mechanic, levels, boosters, rewards, player experience, and an accurate ads/purchases disclosure.
- Store each full translation in the `descriptions` object keyed by the same exact language code as the language dropdown. The 31 currently supported codes are: en, ru, ar, de, es, fil, fr, hi, id, it, ja, ko, ms, nl, pl, pt-BR, th, tr, uk, vi, zh-CN, zh-TW, sv, nb, da, fi, cs, ro, hu, el, he.
- Display the translation with `renderDescription(lang)`; keep `lead` on paragraph 1 and `disclosure` on paragraph 8. Set right-to-left text direction for `ar` and `he`. Fall back to English only if a translation is missing.
- Never leave `#full-description` empty in the source HTML. Pre-render all eight English paragraphs as visible HTML so that content remains if JavaScript fails. The language script replaces them when available.
- Preserve icon, screenshot, support, legal links and site styling during a description-only update.
- Verify 31 keys, eight nonempty paragraphs per language, Arabic/Hebrew direction and static HTML fallback after edits.

Reuse this specification for future Agentik Studio games.
