# What's new in HorizonOS

Newest build first. PTB builds are numbered `<version>-ptb.<build>`; the
same notes appear on the update screen in the app when a build is offered.

## 0.1.15-ptb.1 — 2026-09-13

- A blueprint the game gives no display name shows its internal key, marked as such, instead of a placeholder string.
- Distance is audible now. A station a few gigameters away arrives with a faint static under the voice; ten out, the band narrows and the static rises; past twenty, the voice breaks up in dropouts and flutter; near the 40 Gm horizon it is fragments under the noise. Under 1.26 Gm it is exactly what they sent. This follows the Link Protocol's own coherence model, the same one that drives the signal meter.
- Each radio's meter now shows how far away the station it is hearing is, worked back from the coherence score — "degraded 42% · ≈ 10 Gm".
- Range is only scored between two stations that have both run /showlocation. When that isn't the case the meter reads "no fix" instead of a misleading "degraded 75%", the voice plays clean, and the Radio screen says to run /showlocation.
- Powered radios carry a faint receiver hiss between transmissions, and a short squelch tail when a station unkeys, so a live channel no longer sounds like a dead speaker. Both follow the radio's own volume and ear, not its squelch.
- Settings › Audio has a "Link range effects" switch for all of the above. Off, every transmission plays clean and the radios are silent between them; the meter still shows the zone.

## 0.1.14-ptb.38 — 2026-09-12

- Keeps the Blueprints screen working with Atlas's new item catalogue, which now comes from the game files and grades items with a number instead of a letter.

## 0.1.13-ptb.37 — 2026-09-12

- New Blueprints screen: search the game's 1,608 blueprints, open any of them to see which contracts or reputation tiers award it (with the odds), what it costs to craft, and whether you already hold it. Filter by held / not yet and by whether a mission is known to award it.
- The agent now passes the game's on-screen notifications to Atlas, which records the blueprints you receive in game — that is what the Blueprints screen's "earned" marks come from. Blueprints you already received are picked up from your existing game log the first time the new agent runs. You can also mark one by hand.

## 0.1.12-ptb.36 — 2026-09-12

- Voice settings say "Link Protocol", the name you know it by, instead of an internal one.

## 0.1.11-ptb.35 — 2026-09-11

- No changes for players. Release bookkeeping only.

## 0.1.10-ptb.34 — 2026-09-11

- No changes for players. A fix to how release notes are published, and the first build to prove it end to end.

## 0.1.9-ptb.33 — 2026-09-11

- The update screen now tells you what a new build changes, and every build's notes are collected at github.com/apexstarcomm/horizonos-releases/blob/main/CHANGELOG.md.

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
- Voice goes through Link Protocol at link.apexstarcomm.space by default on new installs.
- On Linux, /showlocation is read from the Wayland clipboard too.

## 0.1.2-ptb.25 — 2026-09-03

- Opening the interface at a direct address like /waypoints from another device no longer fails.

## 0.1.2-ptb.24 — 2026-09-03

- A rebuild of ptb.23 with no visible changes.

## 0.1.2-ptb.23 — 2026-09-03

- The high-resolution map textures are fetched from the web as you need them instead of shipping in the installer, which is about 300 MB smaller.

## 0.1.2-ptb.22 — 2026-09-03

- The first public test build with an installer. A setup screen on first launch, the agent in the tray with the pairing code a click away, automatic updates on both channels, and the agent reachable from a tablet or laptop on your LAN (switched on in setup).
