# What's new in HorizonOS

Newest build first. PTB builds are numbered `<version>-ptb.<build>`; the
same notes appear on the update screen in the app when a build is offered.

## 0.1.8-ptb.32 — 2026-09-11

- Tap your current location in the header to drop a waypoint right where you are. That's the third way to mark your position, next to the "You" marker on the map and the Waypoints page.

## 0.1.7-ptb.31 — 2026-09-11

- Mark where you are: after running /showlocation in game, tap the "You" marker on the map or "Mark my position" on the Waypoints page to drop a waypoint at your exact spot. It's named after the nearest place and notes how old the fix was and how high up you were.
- The header names your system as soon as a position resolves, instead of saying "No position" while the map already shows you.

## 0.1.6-ptb.30 — 2026-09-11

- The Star Map opens straight on the surface view — the one you use in flight — on the planet with the most mapped places in your system, instead of an empty rock in Nyx.
- The map now fills the whole panel (it was drawing in the top third), and the Pyro and Stanton buttons work before you've opened that system.
- Place names no longer pile on top of each other or cover their neighbours' markers, and they sit on whichever side has room.
- On a tablet: press and hold anywhere on the map does what right-click does, tapping near a marker picks the nearest one, holding a radio preset stores the current frequency, and push-to-talk works under a thumb.
- Radio panel controls are bigger and say what they do — ON/OFF, REMOVE, LEFT/BOTH/RIGHT — and the first radio you add is ready to transmit without a second click.
- The status lights say what they mean: AGENT is the link to the game PC, and IN GAME, MENU or NO GAME is the game itself. The old GAME LIVE showed green with the game closed.
- The map's filter button says what it's hiding, like HIDING NATURAL · OTHER, instead of "5 OFF".
- Settings are written in plain language, and a couple of developer toggles are gone.
- Empty screens tell you the one thing to do next.
- Removed for now: the search box and SET button in the header, and the System and Body map views. Settings is in the bottom bar on tablets.

## 0.1.5-ptb.29 — 2026-09-10

- Updating shows a download screen with progress instead of installing in silence.

## 0.1.4-ptb.28 — 2026-09-09

- In-game overlay: a small panel over the game showing the bearing and distance to your destination, from your last /showlocation. Turn it on under Settings › In-game overlay; the game needs to run in borderless windowed mode.
- Your destination now lives on the agent, so it survives closing the interface and shows on every device you've paired.

## 0.1.3-ptb.27 — 2026-09-07

- The mic meter says "silent" and names the likely cause instead of showing -inf.

## 0.1.3-ptb.26 — 2026-09-07

- Radio voice is high quality only now — full-band, with your voice isolated from the room before it leaves your machine — and there's an Audio page in Settings for the input and output device, gain, volume, voice isolation and a mic test.
- Voice goes through Logos at link.apexstarcomm.space by default on new installs.
- On Linux, /showlocation is read from the Wayland clipboard too.

## 0.1.2-ptb.25 — 2026-09-03

- Opening the interface at a direct address like /waypoints from another device no longer fails.

## 0.1.2-ptb.24 — 2026-09-03

- A rebuild of ptb.23 with no visible changes.

## 0.1.2-ptb.23 — 2026-09-03

- The high-resolution map textures are fetched from the web as you need them instead of shipping in the installer, which is about 300 MB smaller.

## 0.1.2-ptb.22 — 2026-09-03

- The first public test build with an installer. A setup screen on first launch, the agent in the tray with the pairing code a click away, automatic updates on both channels, and the agent reachable from a tablet or laptop on your LAN (switched on in setup).
