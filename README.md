# Mage Arena

Mage Arena is a colourful gothic, top-down browser action game about a persistent wizard battling through increasingly difficult arena rounds.

Play the current hosted build: [mage-arena.morganmwj.chatgpt.site](https://mage-arena.morganmwj.chatgpt.site)

## Current features

- Sunstone Colosseum and Moonfall Graveyard arenas
- Ten increasingly difficult combat rounds
- Charged firebolt basic attack
- Directional shield with perfect-parry knockback
- Summon Golem, Vortex, drawn Vine Wall, and Teleport spells
- Health, armour, mana, XP, levels, and persistent browser saves
- Passive talents and individual spell mastery upgrades
- Animated player, enemies, spellcasting, and golem combat
- Spell slots that unlock as the character levels

## Run locally

Mage Arena has no build step or package dependencies. It only needs a small local web server.

### Python

From the repository directory, run:

```bash
python -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser.

On Windows, if `python` is unavailable but the Python launcher is installed, use:

```powershell
py -m http.server 8000
```

### Other local servers

You can also use an editor extension such as Live Server, or any static-file server that serves the repository root. Opening `index.html` directly may work, but a local HTTP server is recommended for consistent browser behaviour.

## Controls

| Control | Action |
| --- | --- |
| `W` `A` `S` `D` | Move |
| Mouse | Aim and choose spell locations |
| Hold left mouse | Charge firebolt |
| Release left mouse | Cast firebolt |
| Hold `Q` | Maintain directional Arcane Shield |
| `1` | Summon Golem |
| `2` | Conjure Vortex |
| `3`, then click-drag | Draw a Vine Wall |
| `4` | Teleport toward the cursor |
| `Esc` | Pause or cancel spell targeting |

Shielding continuously drains mana. Raising the shield just before an enemy strike performs a perfect block, damaging and knocking back nearby enemies.

## Saving

Character level, XP, perk points, and talent upgrades are stored in the browser's local storage. Saves are local to the browser and device being used.

## Project structure

```text
index.html   Game interface and menus
styles.css   Interface and presentation styles
game.js      Game loop, rendering, combat, progression, and saving
```

## Development status

This is an early playable foundation intended for continued expansion. Planned areas include additional enemy types, equipment and enchanted rewards, arena obstacles, more slotted spells, bosses, and deeper talent branches.
