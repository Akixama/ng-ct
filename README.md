# NG-CT — Timeline Fighters

A 16-bit street fighting game starring nine people from the X timeline. Every fighter's head is their profile picture, and every move is built from what they actually post.

**Play it:** https://ng-ct.vercel.app

## Modes

- **Arcade**: pick a fighter and beat the other eight in a row. The CPU gets tougher every stage.
- **VS CPU**: one fight against the CPU on Easy, Normal or Hard.
- **2 Players**: two people on one keyboard.

Fights are best of three, with 99-second rounds.

## Controls

| | 1 player | 2 players (P1 / P2) |
|---|---|---|
| Move / jump | `A` `D` `W` or arrows | `WASD` / arrows |
| Block | hold `S` | hold `S` / `↓` |
| Punch / kick | `J` `K` | `F` `G` / `,` `.` |
| Special | `L` (hold `S` for the second one) | `H` / `/` |
| Super | `I` | `T` / `;` |

On phones, on-screen buttons appear during a fight.

**Moves everyone has**
- **Combos:** `J J K` (1-2-Kick), `J J J` (Uppercut launcher), `K K` (Roundhouse), `J K` (Sweep).
- **Cancels:** any landed hit can be cancelled straight into a special or the super.
- **Low attacks:** hold down and press `J` for a low jab, or `K` for a knockdown sweep.
- **Throw:** forward + `J` up close. It can't be blocked.
- **Guard break:** forward + `K` is a slow overhead that goes through blocks.
- **Dash:** double-tap forward to dash in, or back to back-dash out.

## Roster

| Fighter | Special | ↓ + Special | Super | Passive |
|---|---|---|---|---|
| **Onepeter** @Onepeterrr | Callout | Diamond Hands | 18-Hour Lock-In | Knows What To Do |
| **Skroot** @skrootimburg | Send Floki | Bonding Curve | Doctor's Orders | Last Account |
| **Promise** @sol_promise | $100 Tip | Casino Spin | Giveaway Rain | Big Win |
| **Dave** @solana_dave2 | Dog Wif Hat | Cooking Behind The Scenes | 50x Long | Incredibly Early |
| **Milla** @millw11488 | Merry Men Volley | Sakura Bloom | Force Push | Audited |
| **Hate** @hate_ofx | Going Lowkey | Ape Big | Making It Big | Never Give Up |
| **Exit Liquidity** @exittliquidity | Cape Dash | New Toy | 7 Trench Warriors | Exit Liquidity |
| **Ev** @xeverade | BTC To 69k? | Wasted | End Of The World | Knows Alpha |
| **Karo** @karoblaq | Click Click Click | Chicken Change | Calm | Never Stop Clicking |

Every fighter also has five stats (Health, Speed, Power, Defense, Meter gain), and each one changes how much damage they deal, take and how fast their meter fills. The character select screen in the game shows full descriptions and damage numbers.

## How it's built

It's one static `index.html`: no build step and no dependencies apart from Google Fonts. Everything is drawn on `<canvas>`:

- **Fighters:** procedural cel-shaded sprites drawn at 480×270, with an SVG alpha-threshold filter that gives them hard pixel edges.
- **Heads:** each profile picture in `pfp/` is cut out along a hand-traced outline.

To run it locally, serve the folder with any static server. For example:

```
python -m http.server
```

Every push to `main` deploys automatically to https://ng-ct.vercel.app through Vercel.

## Credits

The profile pictures belong to their owners on X and are used here as a fan tribute to those accounts. If you're one of them and want your picture changed or removed, open an issue.
