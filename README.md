# One More Year: the website

A single static page for the game, in the game's own look: the dark of its start, the album paper on
the desk, the family newspaper, prints with faces drawn by the game's portrait code. Plain HTML and
CSS, no build step, no scripts.

## Publish

Live at https://onemoreyear.joakimfrodin.com since 2026-11-16, on the home server
(`/srv/apps/onemoreyear/`, see `C:\Users\joaki\Documents\hemmaserver\README.md`). GitHub Pages is not used.

1. Upload only the files for the page, never `.git` or `README.md`:
   `scp -r index.html style.css playtest.json fonts img joakim@192.168.1.114:/srv/apps/onemoreyear/site/`
2. Cloudflare keeps CSS for 4 hours, so raise `?v=N` on `style.css` in `index.html` whenever it changes.
3. Push to GitHub too. The playtest build reads the newest version from `playtest.json` on GitHub
   (`raw.githubusercontent.com/jfrodin/OneMoreYearWeb/main/playtest.json`), not from the home server.

## Where the pictures come from

All of it comes from the game (`E:\Dev\Spel\OneMoreYear`), so the page always looks like the game:

| File | Made with |
|---|---|
| `img/mark_face.png` | `Godot --path game -- --icon=PATH --face=480` (the maker's face, in the game's inks) |
| `img/icon.png` | the game's icon, `game/brand/icon.png` (`--icon=PATH`) |
| `img/prints/print_NN.png` | `Godot --path game -- --prints=DIR` (people from the game's own families) |
| `img/shots/*.jpg` | `Godot --path game -- --screenshots=DIR`, scaled to 1280 px |
| `img/desk_wood.jpg`, `img/paper_fibres.png` | the game's textures, ambientCG (CC0) |
| `fonts/*` | the game's typefaces, SIL Open Font License (the licences are next to them) |

No AI-generated images, as in the game.

## To do

- "In development" at the top: make it a "Wishlist on Steam" button once there is a store page.
