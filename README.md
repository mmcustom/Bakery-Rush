# 🧁 Bakery Rush 🥧

A Tapper-inspired arcade game: run a bakery counter, slide desserts down to customers, and catch the empty plates before they crash. Built with [Phaser 3](https://phaser.io/), bundled to run entirely offline as a single static page.

![Bakery Rush screenshot](screenshot.png)

## Play it

No build step, no server, no install. Just open `index.html` in a browser.

```
git clone <this-repo-url>
cd bakery-rush
open index.html   # or double-click it, or drag it into a browser tab
```

Everything the game needs (Phaser, all art) is bundled locally, so it also works fine opened directly as a local `file://` page with no internet connection.

## How to play

Click a counter lane — or press `1` / `2` / `3` — to send the baker there. If a customer is waiting, he serves them; if a plate is coming back, he catches it before it crashes. He can only be at one counter at a time, so timing matters.

- **Cupcake Counter** — fast, straightforward orders.
- **Donut Counter** — orders come two at a time.
- **Pie Counter** — needs a moment to bake before it can go out.

The day runs in three phases — 🌅 Morning Prep, 🔥 Lunch Rush, 🌙 Closing Time — with special customers showing up as things heat up:

- 👑 **VIP** — orders two at once, less patient, pays big.
- 🔍 **Critic** — a miss costs double, a success pays double.
- 👥 **Rowdy Group** — another one arrives the instant this one leaves.

Customers get less patient the longer the day goes on — forgiving early, tighter by closing time.

## Tech

- [Phaser 3](https://phaser.io/) (bundled in `phaser.min.js`, no CDN dependency)
- Plain HTML/CSS/JS, no build tooling — the whole game is `index.html`
- All art in `assets/` is embedded into the page as base64 at load time via Phaser's Texture Manager, so it works when opened directly as a local file

## Project structure

```
index.html       game code, markup, and styling
phaser.min.js     bundled Phaser 3 library
assets/           dessert, character, and background art
screenshot.png    for this README
```

## Credits

Art by Mike. Built with [Claude](https://claude.com).
