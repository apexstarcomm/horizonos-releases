# HorizonOS

A companion interface for Star Citizen. An **agent** runs on the machine
with the game on it — tailing `Game.log`, watching the clipboard for
`/showlocation` coordinates, holding your UCI (Aegis) session, and owning
the microphone and headset for voice. An **interface** draws all of that,
and doesn't have to run on the same machine.

This repo hosts built installers and release notes only. The source lives
in a private repository.

## Download

### Stable

[![Latest stable release](https://img.shields.io/github/v/release/apexstarcomm/horizonos-releases?label=stable&style=for-the-badge)](https://github.com/apexstarcomm/horizonos-releases/releases/latest)

### PTB (Public Test Build)

[![Latest PTB release](https://img.shields.io/github/v/release/apexstarcomm/horizonos-releases?include_prereleases&label=PTB&style=for-the-badge)](https://github.com/apexstarcomm/horizonos-releases/releases)

Stable and PTB install side by side under separate names, so running one
never disturbs the other. PTB gets new features first, in exchange for
occasional rough edges.

## Installing

1. Download the installer `.exe` from a release above.
2. Run it — no administrator rights needed, it installs to your own user
   profile.
3. Launch it from the Start Menu.

## What's inside

- **Atlas** — real-time navigation: your live position and system, a
  zoomable star map with terrain and water overlays, distance measuring,
  and quick search across systems, bodies, and points of interest.
- **Radio** — encrypted, frequency-based voice comms, scoped per star
  system.
- Sign-in is a one-time UCI (Aegis) device-code login that covers every
  device you pair afterward.

## Two ways to run it

- **One machine.** Install HorizonOS on the same PC as Star Citizen — it
  runs as both the agent and the interface together.
- **Two machines.** Run the agent on the gaming PC and the interface
  anywhere else on your LAN — a laptop, a tablet's browser, a second
  monitor. They pair over a one-time 6-digit code, entered once per
  device.

## Auto-updates

Both channels can check for and install updates from this repo, signed
against a key kept out of the source tree entirely. If a build doesn't
prompt you for a newer version yet, grabbing the latest installer above
always works too.

## System requirements

- Windows 10/11, 64-bit
- Microsoft Edge WebView2 Runtime (already present on most up-to-date
  Windows installs — the installer will ask if it's missing)

## Status

HorizonOS is early and under active development, especially on the PTB
channel — expect rough edges. [Open an issue](https://github.com/apexstarcomm/horizonos-releases/issues)
if something breaks.
