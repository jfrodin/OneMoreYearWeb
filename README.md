# One More Year: the website

A single static page for the game, in the game's own look: the dark of its start, the album paper on
the desk, the family newspaper, prints with faces drawn by the game's portrait code. Plain HTML and
CSS, no build step, no scripts.

## Publish on GitHub Pages

1. Create an empty repository on GitHub, for example `OneMoreYearWeb`, and push this folder to it:
   `git remote add origin https://github.com/jfrodin/OneMoreYearWeb.git` and `git push -u origin main`.
2. On GitHub: the repository, Settings, Pages, Source "Deploy from a branch", branch `main`, folder `/`.
3. The page is at `https://jfrodin.github.io/OneMoreYearWeb/` after a minute.
4. Later, a domain of your own (for example onemoreyeargame.com): add it under Settings, Pages,
   Custom domain, and point the domain's DNS at GitHub Pages as GitHub describes there.

## Where the pictures come from

All of it comes from the game (`E:\Dev\OneMoreYear`), so the page always looks like the game:

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

- "Coming to Steam": a link to the store page once there is one.
