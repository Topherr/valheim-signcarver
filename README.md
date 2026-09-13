# Valheim Sign Forge

A single-page tool for making emoji chest labels on Valheim signs, no mods required.
Pick emoji, colors and sizes per line, then copy the rich-text markup and paste it onto a sign in-game.

Based on the technique from [this r/valheim guide](https://www.reddit.com/r/valheim/comments/11v5qg1/quick_guide_on_making_emoji_signs_pc_no_mods/):
`<size=N>` and `<#rrggbb>` tags apply to everything after them, and `<br>` breaks lines.

## Use it

Open `index.html` in a browser, or visit the GitHub Pages site for this repo.

## How signs render emoji

- The game draws emoji from a bundled single-color font (Noto Emoji), so every emoji takes whatever color tag is in force. The preview and palette use the same font.
- Coverage stops at Emoji 15.0. Emoji added in 2024 or later, and combined emoji (skin tones, flags, joined pairs), show as boxes.
- The tool drops the `U+FE0F` "emoji style" selector; the game ignores it and it costs a character.
- Colors are written as 3-digit hex where possible (`<#f93>` instead of `<#ff9933>`).
- Signs hold 50 characters including tags. Most emoji count as 2.

The palette is grouped by what people keep in chests: tools, weapons, armor, seeds, food, meads, ores, materials, creatures, places, and marks. Hover a tile for the item it stands for.
