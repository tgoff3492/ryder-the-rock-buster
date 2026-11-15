# Ryder the Rock Buster — Design Notes

## The idea (from RJ)
- You're a guy (Ryder) fighting **rock monsters** with a **gun**
- **Levels** that get harder
- **Upgrades** you pick up make the gun more powerful and do more damage
- Upgrades add **special abilities** that make the gun look cooler when it fires

## Design rules
1. **A 6-year-old should never get stuck.** No game over, retries keep upgrades, auto-aim, slow monsters in Kid Mode.
2. **Every upgrade has to be visible.** The gun gets longer, changes color, glows, gets lights, and grows extra barrels and fins. Each bullet type has its own look and trail.
3. **Stuff should feel crunchy.** Screen shake, rock chunks, comic words ("CRUNCH!", "KABOOM!"), and sounds on every hit.
4. **Controls are arrow keys + SPACE** (made for a Mac laptop with a trackpad).

## How the code is organized (`index.html`)
| Section | What's in it |
|---|---|
| `UP` | Every power-up: icon, color, name, description |
| `MT` | Every rock monster type: size, health, speed, color, special behavior |
| `LEVELS` | The 10 levels: name, background theme, how many rocks, which kinds, boss settings |
| `fire()` / `hitMonster()` | What the gun does and what each special power does when it hits |
| `chooseUpgrade()` | Picks which prize drops (cool specials first, then power/speed) |
| `drawGun()` / `drawBullet()` | How the gun and bullets look for each upgrade |
| `bossAI()` | The Rock King's attacks: a ring of thrown rocks and summoning pebbles |

### Easy things to tweak
- **Make it easier or harder:** `speedMul()` and `maxHp()` set monster speed and number of hearts for each mode
- **Add a level:** add a line to `LEVELS`
- **Change how many prizes drop:** the `drops` number in each level
- **New monster:** add it to `MT`, then use its name in a level's `mix`

## Ideas for next time (ask RJ!)
- [ ] Pick a different hero (colors, hats)
- [ ] New rock monsters: a sneaky invisible rock, a giant rock snake, a flying rock bat
- [ ] More guns: freeze ray, bubble gun, laser sword
- [ ] A shop between levels to spend score on upgrades
- [ ] Two-player mode on one keyboard (WASD + arrows)
- [ ] Music
- [ ] Bigger maps that scroll
- [ ] Secret level
