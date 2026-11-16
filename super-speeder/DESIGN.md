# Weston Super Speeder — Design Notes

## Who it's for
Weston (about 3). It should be fun for a little kid who's just learning arrow keys, and still fun for a grown-up racing against him.

## Design rules
1. **Weston can't lose.** In Little Kid Mode the car follows the road by itself, computer cars stay just behind him, and nothing can knock him off the road. Every race ends with a trophy and confetti.
2. **Nothing needs reading.** Big colorful buttons, horns, flashing lights, and comic words ("ZOOOM!", "HONK!!", "SPLAT!") do the explaining.
3. **Holding one key is enough.** Any arrow key makes the car go. Prizes and nitro go off by themselves in Little Kid Mode.
4. **Grown-ups get a real race.** Big Kid Mode has real steering, braking, grass that slows you down, and computer cars that try to win.
5. **Same rules as the arcade:** arrow keys + SPACE, everything visible, crunchy sounds.

## How the code is organized (`index.html`)
| Section | What's in it |
|---|---|
| `VEH` | Every ride: name, colors, horn, top speed, how much grass slows it |
| `drawVehicle()` | How each ride is drawn from above (pointing right) |
| `DECALS` / `drawDecal()` | Stickers and how many ⭐ each one needs |
| `ITEMS` / `useItem()` | The prize-box powers and what they do |
| `TRACKS` | The 5 tracks: the points the road goes through, boost pads, prize boxes, stars |
| `SCENERY` | Trees, palm trees, snowmen, lollipops, craters for each track theme |
| `driveRacer()` | How cars move: Little Kid and computer cars glide along the road; Big Kid cars steer freely |
| `aiSpeed()` | How fast the computer cars go and how they stay behind a Little Kid |
| `finishRace()` | Results, stars, and unlocking tracks and stickers |

### Easy things to tweak
- **Speed:** `KID_V` (Little Kid) and `BIG_V` (Big Kid)
- **Laps:** set in `setupRace()` (2 for Little Kid, 3 otherwise)
- **New track:** add an entry to `TRACKS`. The points go clockwise around the screen, and the first point is the start line (put it on a straight part). Keep the road at least ~110px away from itself.
- **New ride:** add it to `VEH`, then add a drawing for its `kind` in `drawVehicle()`
- **Sticker prices:** the `need` numbers in `DECALS`
- **Prize odds:** `rollItem()`

Unlocks and settings are saved in the browser (`localStorage` key `speeder_save`).
To reset everything, open the browser console on the game and run `localStorage.removeItem('speeder_save')`.

## Ideas for next time (ask Weston!)
- [ ] More rides: school bus, tractor, dump truck, ambulance, rocket car
- [ ] Jump ramps
- [ ] A track that goes over a bridge
- [ ] Weather: rain puddles, snowfall
- [ ] Music
- [ ] Pick the computer cars' colors
