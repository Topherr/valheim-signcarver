# Valheim Signcarver

A single-page tool for making emoji chest labels on Valheim signs, no mods required.
Pick emoji, colors and sizes per line, then copy the rich-text markup and paste it onto a sign in-game.

Based on the technique from [this r/valheim guide](https://www.reddit.com/r/valheim/comments/11v5qg1/quick_guide_on_making_emoji_signs_pc_no_mods/):
`<size=N>` and `<#rrggbb>` tags apply to everything after them, and a line break starts a new line.

## Use it

Open `index.html` in a browser, or visit the GitHub Pages site for this repo.

## How signs render text

- **Sizes are absolute.** A size-14 capital spans the plank top to bottom, and lines add up, so an emoji at 6 over a word at 3 fits on the plank. Leave every size blank and the game fits the text to the plank on its own, up to about size 8.
- **The sign centers its text block on the plank.** Anything taller than the plank hangs off above and below. Blank lines below the label push it up; blank lines above push it down.
- **The sign font is capitals only.** Lowercase renders as capitals.
- **Emoji are single-color.** The game draws them from a bundled Noto Emoji font, so every emoji takes whatever color tag is in force. The preview and palette use the same font. Coverage stops at Emoji 15.0; emoji added in 2024 or later, and combined emoji (skin tones, flags, joined pairs), show as boxes.
- **Line breaks.** A typed `\n` breaks a line for 2 characters. `<br>` also works and costs 4; there is a checkbox for it.
- **Colors** are written as 3-digit hex where possible (`<#f93>` instead of `<#ff9933>`), and the `U+FE0F` emoji-style selector is dropped since the game ignores it.
- Signs hold 50 characters including tags. Most emoji count as 2.

A search box finds any single-glyph emoji by its Unicode name or its Valheim label ("eye", "lox", "draugr"). The palette is grouped by what people keep in chests: tools, weapons, armor, seeds, food, meads, ores, materials, creatures, places, and marks. Hover a tile for the item it stands for.
