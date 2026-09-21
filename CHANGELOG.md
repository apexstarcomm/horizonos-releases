# What's new in HorizonOS

Newest build first. PTB builds are numbered `<version>-ptb.<build>`; the
same notes appear on the update screen in the app when a build is offered.

## 0.1.15-ptb.11 — 2026-09-21

- Push-to-talk and the radio next/previous keys can now be bound to a modifier combo — hold Ctrl, Alt or Shift together with another key — instead of only a single key.
- Keybindings can now use most of the keyboard, not just letters, digits and function keys — punctuation, Tab, Enter, the arrow and navigation keys, and the full numpad are all bindable now.
- Added an opt-in diagnostics toggle (off by default, in the setup screen) that sends anonymous performance traces through your account's relay — nothing is sent unless you turn it on.
- The error toast and the red "error" status dot (audio input, blueprints, waypoints) now actually show red instead of rendering with no color at all.
- Every dropdown (Settings, the market panel's ship and origin pickers, the report sheet) now renders with its intended dark styling on Linux instead of a plain native combo box.

## 0.1.15-ptb.9 — 2026-09-18

- The agent now refuses to start a second time on the same machine instead of silently starting halfway (microphone, clipboard watcher and all) and then dying late, near-invisibly, on a port conflict — a real session showed exactly that: `/showlocation` stopped capturing with nothing in the log to say why.
- A clipboard read failure (something else holding it, a permissions change) is now logged instead of silently discarded — it used to be indistinguishable from `/showlocation` simply not being run.

## 0.1.15-ptb.8 — 2026-09-18

- If the agent's UCI session drops while you're flying, HorizonOS now takes you back to the sign-in screen instead of just showing "agent isn't logged into UCI yet" on whatever you were looking at.
- The report sheet now says when it's still checking what the community has already reported, instead of a field looking the same whether nothing's been reported or it just hasn't answered yet.
- Screen readers now hear a short, clear name for the blueprint list's rows, the radio tune dialog's channel-directory rows, the header's current-location control, and push-to-talk — instead of every line of their content run together as one.
- Search and the report sheet's close buttons now say "Close" instead of "esc" — Escape itself still works either way.
- The agent picker now closes on Escape too, once there's already an agent to fall back to.
- Radio: the Tune dialog's preset tiles now show which preset matches the frequency you're on, the same as the compact panel behind it, and its close button says "Done" instead of "esc".
- Waypoints: pressing Escape now backs out of editing a waypoint or a "delete for good?" confirmation, the same as everywhere else Escape backs out of something.
- A blueprint's recipe now says "Checking price…" for an ingredient it hasn't priced yet, instead of leaving the row blank the same way it looks once nobody's found selling it.
- Radio: pressing Escape now cancels a "remove this radio" confirmation, the same as everywhere else Escape backs out of something.
- Market: the "Best move right now" card announces as one short line for a screen reader — the rate and which panel it jumps to — instead of the whole card's text read out as its name.
- Settings › Appearance now calls its colour picker "Livery" and offers eleven manufacturer paint schemes — Aegis, Anvil, Crusader, Drake, Gatac, Greycat, Mirai, MISC, MobiGlass, Origin and RSI — alongside the original Amber, Cyan and Orange, all in one list.
- Waypoints: a row is now the click target for jumping to it on the map, the same as every other list in the app, instead of a separate Map button — Edit and Delete stay as their own smaller buttons. The header's three actions are sized like every other action button in the app instead of standing taller than the rest of the page.
- Waypoints now uses the same status shapes as everywhere else — a dot for synced, a ring for not-yet-synced, a dashed ring for an imported read-only one — instead of its own hand-drawn squares, and the header's actions sit behind a divider from the title.
- Report buttons are now a quiet pencil mark instead of a labelled button, and a blueprint's mission list wears one per mission instead of one per variant — the same reports, with far less shouting on screen.
- On Linux, pinching on a touchpad no longer zooms the whole window — two-finger scroll still zooms the map underneath your cursor, the same as everywhere else.
- Small captions and labels are a touch brighter, clearing the readability floor they always claimed to meet.
- The livery you pick in Settings now reaches every screen, including the pairing-code box and the "Can't reach the agent" notice, which used to stay amber whatever you chose.
- Every status light now has a shape as well as a colour: a dot for live, a ring for stale, a dashed ring for offline and a diamond for an error.
- Settings › Appearance has a new Status colours switch. Colour-safe swaps the green and yellow status lights for blue-green and gold, which stay apart under red-green colour blindness; the shapes are the same either way.
- A place held by an outlaw faction that fires on anyone now also carries a ring around most of its markers, so the map still says who holds it if you can't tell red from green; the key shows the same mark.
- The Radio page no longer calls the transmitting radio "the amber radio" — it says "the highlighted radio", whatever livery you chose.
- Blueprints: every row now shows held-or-not as a shape as well as a colour, and a blueprint row can be opened from the keyboard, not just a click.
- A blueprint's recipe now says where to buy each catalogue-item part and for how much, cheapest first, with a Trace button straight to it; raw materials that aren't sold anywhere are left as they were.
- Blueprints: hovering or keyboard-focusing a row is now clearly highlighted — it used to barely change colour at all.
- Blueprints: the category list is now a dropdown grouped by kind, like the Star Map's filter, showing your progress (like "Size 2  0/116") instead of a long row of wrapping chips.
- Blueprints: a row you already hold now says when you earned it instead of repeating how to earn it, which no longer matters once you have it.
- Market has a jump strip pinned under the header — Refilled, Runs and Loops each show their count and best figure, and a click scrolls straight to that panel instead of a long scroll through all three.
- Market's rows now lead with the one number that matters — the rate or SCU gained — with the route on its own line and the supporting math (capital, decay, timing, age) grouped underneath instead of crowded onto one wrapping line.
- A terminal's commodity board carries the same change: the price leads each row on its own line, with room, fill, the 30-day band and the quote's age grouped underneath.
- Market leads with a "Best move right now" card — the single best figure across Refilled, Runs and Loops, in plain words, so the page states its own answer instead of leaving the comparison to you.
- Market's "From here, in this ship" controls now start collapsed on every screen size, since the summary line already says what they're set to.
- The "Best move right now" card now shows how old its own figure is, the same age every other number on the page wears.
- The jump strip's Refilled pill now shows a rate in aUEC/h, like Runs and Loops, instead of SCU gained, so all three line up for comparison.
- A loop row's disclosure button now says "More", matching every other row, instead of "Legs".
- Market now says plainly when the agent can't be reached, instead of the browser's own "Failed to fetch".
- Market now says once, clearly, when no terminal is picked as your origin yet, instead of repeating the same instruction inside all three panels below.
- Market's jump strip and every row's disclosure button are now plain, honestly-labelled controls — a screen reader no longer hears them announced as tabs they can't actually operate, and jumping to a panel now actually moves keyboard focus there, not just the scroll position.
- Every "More"/"Less" and "Show rows"/"Hide" button on Market now tells a screen reader whether it's open or closed.
- Market's "From here, in this ship" controls now open by themselves the first time something's still missing, instead of leaving the fix behind a small "Change" button the page just told you to find.
- What the whole system can sustain is now a real switch on Market — click P25, Median or P75 and every figure on the page recomputes at that rate, instead of it only being a read-out.
- A loop that wins "Best move right now" now says so honestly — "best as a one-off" when the second lap doesn't hold up, instead of always claiming it repeats.
- When the agent can't be reached, Market no longer shows two warnings that contradict each other about picking an origin.
- The "Best move right now" card now says how its figure compares to what the system can sustain overall.
- Market's Runs and Loops panels have an "Expand all"/"Collapse all" switch for comparing several candidates at once.
- Refilled, Runs and Loops each show five rows by default with a "Show all" to see the rest, instead of the full list always in view.
- Once "Best move right now" has an answer, only the panel it came from stays open on Market — the other two collapse to their summary line, one click away.
- The Star Map has a locate button next to zoom that centres and zooms in on your last position fix, the same as a locate button on any other map.
- Opening the Star Map's filter or layers menu no longer shoves the buttons next to it sideways.
- The Star Map's legend now trails off with "…" instead of cutting a word in half when the map is too narrow to show it in full.
- Screen readers now hear whether a Star Map filter category is fully on, off, or only partly on, instead of just "button".
- Waypoints: deleting one now asks you to confirm first, since there's no way to undo it.
- Waypoints: the reason "Mark my position" is greyed out now stays on screen instead of only showing on hover.
- Waypoints: clearing a name while editing and hitting Save no longer silently keeps the old name — Save waits until you type one.
- Radio: a preset can now be saved from the keyboard — hold Enter or Space on it, the same as holding a click or a right-click.
- Radio: push to talk can now be pressed and held from the keyboard, not just clicked or bound to a key.
- Radio: removing one now asks you to confirm first, since it can't be undone.
- Radio: the tune dialog now closes on the Escape key, not just its own "esc" button.
- Radio: the "Sql" slider is now called "Gate" — Link Protocol is a digital link with no static for a squelch to listen through, and this always just quieted soft audio, not radio noise.

## 0.1.15-ptb.6 — 2026-09-17

- The sign-in screen now says plainly that HorizonOS is an unofficial fan project, not affiliated with Cloud Imperium Games or Roberts Space Industries, instead of leaving that note tucked away in Settings.
- Each channel now has a fixed download link that always gives the newest build: github.com/apexstarcomm/horizonos-releases/releases/download/ptb/HorizonOS.PTB_x64-setup.exe for the PTB, and the same under stable/HorizonOS_x64-setup.exe once the first stable ships.
- Keybindings now live on their own page in Settings, and switching to the next or previous radio can be bound to a key alongside push-to-talk. The numpad + and - keys can be bound too.
- Rebinding push-to-talk away from its default now actually replaces the default: previously the spacebar could keep working for push-to-talk after a different key was bound to it. Space now only works until you bind or clear the key yourself.
- Mouse side buttons (Mouse4 and Mouse5) no longer navigate the app back or forward once bound to an action.
- Switching surfaces now uses Alt plus a key instead of a bare number, and each surface's key can be changed from the same Keybindings page — this one is remembered on this device only.

## 0.1.15-ptb.5 — 2026-09-15

- The map shows who holds a place. An outpost or bunker held by an outlaw faction that fires on anyone (the Nine Tails bunkers) is drawn in red; one whose guards react to your own standing (HeadHunters, Rough & Ready, Citizens for Prosperity) in yellow; everything lawful looks as it did. The key says which is which, and selecting a place says it in words — "Nine Tails · fires on anyone". Needs an Atlas that carries the field; older ones simply draw nothing new.
- Blueprints you earned before installing HorizonOS are picked up too: on each launch the agent reads the game's rotated logs (logbackups) once, and the other of LIVE and HOTFIX when both are installed, and Atlas marks what they say you received. Each file is read one time; nothing is re-sent on later launches.
- A blueprint nothing awards now says so: "no contract or reputation tier in the current build hands it out", instead of guessing at shops. Blueprints only come from finishing contracts.
- Calibration: a proposal that lands you near your anchor but more than 50 m from its catalogued point can now be accepted. The review says how far off it puts you and lets you judge; it still refuses when some other place is nearer than the one you picked.

## 0.1.15-ptb.4 — 2026-09-15

- Blueprint categories are named in plain words: the filter chips, the catalogue rows and a blueprint's page say "Armor" or "Vehicle weapons · size 3" where they showed the game's own codes. The names come from Atlas, so a category the game adds later reads properly without an app update.

## 0.1.15-ptb.3 — 2026-09-15

- Distance now sounds like a digital link failing, not a radio hissing: past a gigameter the voice narrows and loses resolution, further out packets go missing and frames stutter, and under 1.26 Gm it is exactly what was sent. Nothing plays between transmissions any more — the receiver hiss and the squelch tail are gone.
- A Market surface: from where you are, in the ship you are flying, what is worth carrying right now — and what it will actually pay once the buyer fills up. Runs from the nearest terminal ranked by aUEC per hour with the profit after decay beside the quoted figure, loops with what the second lap pays (and a plain "not repeatable" when demand refills too slowly to fly the route twice), and a strip saying what the whole system can sustain. Every quote wears its age, every projection names the refill model it assumed, and the header says when the quotes last changed.
- The Market's ship defaults to the one your game log names — the log says which ship you are in when you plot a quantum route — with its hold and drive from Atlas where known. Any other ship can be picked from Atlas's own list; where Atlas has no cargo grid for a hull yet, the hold comes from a small table in the app or is typed in, and the row says which. Legal-only, loading class, refill bracket, cross-system, wallet and quote age are controls, each with a sentence on what it changes.
- A "worth flying now" panel lists the sinks that regained room since you last looked at them, with the best source for each. Your looks are kept on this device only; a terminal counts as looked at when you open its board, when you are standing at it, or when you say so.
- Every terminal named on the Market opens its commodity board: what it buys and sells, how much room each sink has left, how full it is against the price curve, the 30-day band and how old each report is. The same board sits on a terminal's page.
- Commodity quotes come from UEX; the surface carries the Powered by UEX badge, linking to uexcorp.space.

## 0.1.15-ptb.2 — 2026-09-13

- The push-to-talk key the agent watches on the game PC can now be set from Settings › Connection on any paired device: click the key and press the one you want, or pick it from a list, and choose hold or toggle. It is saved on the agent and takes effect right away, so every device paired to it sees the same key.
- Mouse side buttons (Mouse4 and Mouse5) can now be the agent's push-to-talk key.
- The -PttKey, --ptt-key and HORIZONOS_PTT_KEY options now only set the key the first time the agent runs; after that the key saved on the agent is the one that counts.
- Changing the push-to-talk key or its mode while transmitting ends that transmission.
- You can now report on where you are. A REPORT button in the header opens a sheet for the nearest catalogued place: say whether it is still there, closed or gone, and confirm or correct its landing pad count, hangars, armistice zone and services; every report is dated by your /showlocation fix. The same sheet shows what other players have reported so far, and flags a value the game's files have since moved away from.
- You can propose a place the catalogue does not carry, from your current fix: a name, a category and an optional description. A reviewer accepts proposals by hand, and the sheet tells you when a catalogued place already sits within a kilometre.
- Buying at a kiosk now reports the price the kiosk quoted, on its own: the agent forwards the game's own shop line to Atlas, which turns it into a community price on that terminal. Your own name is blanked before the line leaves the game PC, and the agent reads nothing else out of it.
- The report sheet now offers everything your fix names — the system, the body and the nearest place — and the same sheet opens from a blueprint's page, from each contract that awards it (the ones the game gives no title can be given one) and from a ship's page, for whatever Atlas takes reports on there: a description, a body's designation, a ship's role, a note on a recipe.
- Both report controls follow the Contribute setting under Settings › Data & honesty; turn it off and they disappear.

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
