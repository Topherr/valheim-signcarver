# Valheim Sign Forge

A single-page tool for making emoji chest labels on Valheim signs, no mods required.
Pick emoji, colors and sizes per line, then copy the rich-text markup and paste it onto a sign in-game.

Based on the technique from [this r/valheim guide](https://www.reddit.com/r/valheim/comments/11v5qg1/quick_guide_on_making_emoji_signs_pc_no_mods/):
`<size=N>` and `<#rrggbb>` tags apply to everything after them, and `<br>` breaks lines.

## Use it

Open `index.html` in a browser, or visit the GitHub Pages site for this repo.

## Notes

- Signs hold 50 characters including tags. Most emoji count as 2.
- Not every emoji renders in-game. If one shows as a blank box, pick an older, more common one.
- The preview is an approximation of the in-game sign.
