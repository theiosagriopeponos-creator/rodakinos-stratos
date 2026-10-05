# What I want (paste this below the line of the Melty Publish prompt)

## The mashup
**Crowbar Escape** (the listing title I chose). The player runs Sonic Adventure 2's City Escape stage as Gordon Freeman. Sonic's attack is replaced by a crowbar swing. The stage plays Half-Life 2 sound effects and music. SA2's own robot enemies stay as they are; Gordon fights them.

- **Host game:** Sonic Adventure 2 (PC). Identify the exact version and install from its folder.
- **Other game:** Half-Life 2 is a **required game**. Gordon's look and the HL2 sounds/music are read from the player's own Half-Life 2 install and converted on their PC; no Valve files ship in the release. That needs a converter written as part of the mod. Early on, run `one_click_check` to confirm Melty accepts a pre-launch or first-launch conversion step, and tell me before building if it does not.
- **Players:** solo only. No multiplayer, so leave `recipe.multiplayer` out.
- **First minute:** the player starts City Escape as Gordon and runs the stage.

## Already decided (do not ask again)
- Gordon replaces Sonic as the playable character.
- Crowbar swing replaces Sonic's attack.
- Half-Life 2 sound effects and music in the stage.
- SA2's own enemies stay; Combine and headcrabs are NOT part of version 1.
- Solo only.
- Listing title: **Crowbar Escape**. Tagline and description are drafts in `design_sheets.json`; update them once the build runs and I approve.
- License: **MIT** for the mod's own code (Valve and Sega content is not included and stays theirs), and **others may remix it**. If a bundled loader or library has its own license, keep it and credit its authors.
- **Screenshot:** you capture it, on my PC, once the mod runs: game window only, showing Gordon's crowbar swing in City Escape. No private windows or tokens. Keep the listing a draft until it exists.
- **No build exists.** You build and test it yourself on my PC; do not wait for one from me. Keep anything source-only or untested clearly labeled.
- Assets come from the player's own Half-Life 2 install, so HL2 is a required game and no Valve files are bundled.
- The crowbar swing replaces Sonic's **Homing Attack** (I let the design assistant pick it). Version 1 aims to keep the game's existing lock-on movement and hit logic and swap only Gordon's swing animation and the HL2 sounds. Confirm that is feasible in the running game and tell me if it is not.

## Open decisions (ask me one at a time, with two to four ideas each)
1. **Gordon's jump pose.** Sonic's jump is a spin ball. Offer me two or three options for how Gordon should jump.
2. **Gordon everywhere, or City Escape only?** File replacement may change Sonic in every stage. Tell me what the loader allows before I choose.
3. **Which HL2 track plays as the stage music?** Check the real track list in my HL2 install first, then offer options by mood.
4. **Credits.** Confirm the author name with me. Plan: Valve (Half-Life 2), Sega / Sonic Team (Sonic Adventure 2), the SA2 Mod Loader / SA Mod Manager authors, and me.

## Files in this folder
`design_sheets.json` is the source of truth. Change the sheet before the code. Unfilled cells are `null`; candidate names marked `to_verify` are guesses and must be checked against the real game files before use. Never invent addresses, file names or enemy names.

## Order of work
1. Connect to Melty. Call `game_info` on both games, and `search_mashups` for them. Tell me in two or three lines what Melty installs by itself, whether either game puts an account at risk (I expect neither does, since both are offline single-player; confirm it), and anything close that already exists.
2. Inspect the SA2 folder. Identify the version and modding route (the SA Mod Manager / SA2 Mod Loader is the established one) and check whether Melty installs it.
3. Run a **preflight** on `design_sheets.json`: list every unfilled cell and every reference that does not resolve. Fix those with me first.
4. Build in this order, testing each step in the running game: (a) sound swap, as proof the route works; (b) crowbar attack hook; (c) Gordon model and animations.
5. Package it, run `inspect_package`, `validate_recipe` and `one_click_check`. Tell me before building anything that cannot work in one click.
6. Capture a real screenshot of the finished mod running (game window only), then create the listing as a draft and ask me to test it in Melty before publishing.

## Rules
- Keep the Melty token out of project files, commits, logs and replies.
- Do not bundle Valve or Sega content unless a license says it can be shared; tell me what you decide and why.
- Ask before anything that costs money.
