# Hunting Run — Prototype08 browser playtest

[Play Prototype08](https://wasiqnkhurshid.github.io/HuntingRunGame-Prototype08/) — no installation or GitHub account required.

Source/build reference: `b6e3c8d6a27b89a07b370ee35f80947ca213c518`. This repository contains the compiled browser game only.
Prototype08 checkpoint: `e62f551e510f3c31de65e0b480454fc286c1dc22`; the only runtime patch restores the pause configuration button.
The private source remains in HuntingRunGame on `codex/prototype08-gameplay-feel`.
Stable Prototype07 remains at https://wasiqnkhurshid.github.io/HuntingRunGame-WebGL/.

## Testing

Choose **FEEL TESTS**, select speed (29/32/35 m/s), camera and shooting profiles, then **START TEST**.
Pause → **TEST CONFIGURATION** changes settings and restarts the same seed.
**RESET P07 VALUES** restores baseline profiles/input/aiming for comparison.
**BACK TO NORMAL** leaves the isolated experiment.

Phone: hold portrait; swipe left/right/up/down; tap Shoot. A second finger can move while Shoot is held.
Desktop: A/D or arrows change lanes, Space/W jumps, S ducks, Enter shoots, Esc pauses.
Mouse swipe moves; a playfield tap shoots. Mouse/keyboard and emulated touch are validated in Chrome.
Extremely fast mouse drags whose press/move/release arrive in one engine frame can be read as taps.

The landing page enables `feel=1` automatically without enabling QA instrumentation.
Experiment rewards/resume snapshots are not saved. A separate IndexedDB filesystem namespace
isolates this site from Prototype07 even though both share the GitHub Pages origin.

## Limitations

WebGL2 and WebAssembly are required. Initial compiled download is about 31.6 MB; mobile loading
and frame rate depend on the device/browser. Physical Android/iPhone and Safari are not validated.
Storage restrictions/private browsing may prevent persistence. Use current browsers and portrait.
The visual bow draw follows the immediate gameplay arrow; exact release synchronization is unfinished.
The configuration screen retains the original LOCAL DEVELOPMENT ONLY label from e62f551.

## Rollback

This site is independent of Prototype07. To stop this experiment, open this repository's
Settings → Pages and unpublish the site. To restore this release after a future update,
restore the files from tag `prototype08-e62f551-playtest` in a new commit on main and push.
Neither operation changes the stable repository/site. Never force-push the stable repository.
