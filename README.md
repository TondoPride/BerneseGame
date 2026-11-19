# Bernese Hazard

*A Good Boy Survival Horror.*

A Resident Evil–style isometric survival-horror game about two Bernese Mountain Dogs, Chuck and Jackson, left home alone on a stormy day, and June, the family cat who may be behind all of it.

The whole game is one self-contained file: `index.html`. There's nothing to install and no build step, and it works offline.

## Play

- **In a browser:** open `index.html`.
- **Online:** every push to `main` builds and deploys the game to GitHub Pages automatically (see `.github/workflows/deploy-pages.yml`). It's playable at `https://tondopride.github.io/BerneseGame/`.
  - One-time setup: in the repo's **Settings → Pages**, set **Source** to **GitHub Actions**.
  - You can also redeploy by hand from the **Actions** tab ("Build & deploy to GitHub Pages" → Run workflow).
- **On a phone:** open the Pages link in landscape. Tap ⛶ for fullscreen, or use Add to Home Screen.

## Stories

| Story | How to unlock | What it is |
|---|---|---|
| **Chuck's Story** (Scenario A) | Available from the start | Rescue Mr. Mally, then go after the Big Bone and face the TurboSuck 9000. |
| **Jackson's Story** (Scenario B) | Clear Chuck's story | The same afternoon from Jackson's side: get Big Red back from the Shop-Vac. Gives the true ending. |
| **June's Story** (Bonus) | Find all 10 catnip mice (5 in each dog's story) | The morning, from the cat's point of view. She walks on furniture, hisses and has a plan. |

A choice in Chuck's story carries over to Jackson's: take the Squeaker Horn, or leave it for him.

**Dev shortcut:** press **U** on the title screen, or tap the title logo 5 times, to unlock all stories.

## Controls

| Action | Keyboard | Controller | Touch |
|---|---|---|---|
| Move | WASD / Arrows | Left stick / D-pad | Left-thumb joystick |
| Run | Shift (hold) | B or trigger (hold) | RUN (hold) |
| Sniff / interact / confirm | E / Enter | A | ACT, or tap |
| Bark (stun) / June: hiss | Space | X | BARK |
| Inventory | Tab / I | Start | BAG |
| Switch inventory tab | Q | LB / RB | Tap the tab |
| Tank controls | T | View / Back | — |
| Sound on/off | M | — | ♪ |

Progress is saved by napping in a dog bed. Saves and unlocks are stored in the browser you play in (localStorage).

## Tech notes

- Plain HTML5 Canvas and JavaScript in one file, with no dependencies.
- Music and sound effects are generated in code with the Web Audio API, so there are no audio files. Each area has its own ominous theme over a low drone that follows the room's key. A tension layer rises when something is chasing you, and the dog-bed save spots keep a calm safe-room theme.
- Supports keyboard, the standard Gamepad API, and touch controls with a fullscreen and landscape layout on phones.
