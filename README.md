# Goff Kid's Arcade 🕹️

Games made for the Goff kids. Pick a game from the menu with the **arrow keys** and press **SPACE** to play.

## ▶ Play it now

**https://tgoff3492.github.io/ryder-the-rock-buster/**

Works in Chrome or Safari on a computer (the games need a keyboard). You can also open `index.html` straight from the folder.

## The games

| | Game | For | What it is |
|---|---|---|---|
| 🪨💥 | [**Ryder the Rock Buster**](rock-buster/README.md) | Ryder (game idea by RJ) | Blast rock monsters, grab gun upgrades, beat the Rock King |
| 🏎️💨 | [**Weston Super Speeder**](super-speeder/README.md) | Weston | Race cars, monster trucks, fire trucks and more around 5 tracks |

In either game, press **Esc** on the title screen (or click **🏠 Arcade**) to come back to this menu.

## How it's set up

```
index.html             ← the arcade menu (the play link opens this)
images/                ← the pictures on the menu
rock-buster/           ← Ryder the Rock Buster (index.html is the whole game)
super-speeder/         ← Weston Super Speeder (index.html is the whole game)
```

Each game is a single HTML file with plain JavaScript and no libraries.

**To add a new game:** make a new folder with its own `index.html`, add a card for it in the arcade's `index.html`, and put a 480×320 picture in `images/`.

## Rules every game follows

1. **Arrow keys + SPACE.** Made for a Mac laptop with a trackpad.
2. **A little kid should never get stuck.** There's always an easy mode, and no "game over" that throws away progress.
3. **Everything you collect shows up on screen.** Upgrades change how things look.
4. **Stuff should feel crunchy.** Sounds, shakes, and comic words on everything.
5. **Sounds are made with code**, so there are no sound files to load.
