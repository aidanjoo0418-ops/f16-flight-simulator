# F-16 Falcon — 3D Flight Simulator

A browser-based 3D F-16 flight simulator built with **Three.js** in a single HTML file — no build step, no install.

**Play:** open `index.html` in any modern browser (or enable GitHub Pages on this repo).

## Features

- **Flight model** — lift/drag curves, stall behaviour, altitude-dependent air density, Mach effects, and a fly-by-wire G limiter (+9 / −3 G, 25° AoA)
- **Engine** — military power and afterburner staging above 80% throttle, with spool-up lag and visible AB flame
- **Fighter HUD** — pitch ladder, flight path marker, heading tape, speed/altitude tapes, Mach, G, AoA, vertical speed, radar altitude
- **Procedural world** — fractal-noise terrain with snow-capped mountains, forests, lakes, clouds, and towns that light up at night
- **Airport** — textured runway with markings, taxiways, hangars, control tower, runway/approach lights and a working **PAPI** glideslope indicator
- **Weapons** — six AIM-9 missiles with smoke trails and explosions
- **Day / sunset / night** cycle, cockpit and chase cameras, synthesized engine and wind audio
- **Landing & crash detection** — touchdown rate in FPM, gear-up landings, terrain impact, PULL UP / STALL / GEAR warnings

## Controls

| Key | Action |
| --- | --- |
| `W` / `S` | Nose down / nose up |
| `A` / `D` | Roll left / right |
| `Q` / `E` | Rudder (steer on ground) |
| `R` / `F` | Throttle up / down |
| `Space` | Fire AIM-9 |
| `B` | Brakes / speed brake |
| `G` | Landing gear |
| `V` | Cockpit / chase camera |
| `N` | Day / sunset / night |
| `P` | Pause |
| `Enter` | Reset on runway |
| `I` / `M` / `H` | Invert pitch / sound / hide help |

**Takeoff:** hold `R` past 80% throttle, rotate with `S` at ~150 knots, then raise the gear with `G`.

## Tech

- Three.js r128 (WebGL), custom sky shader, instanced meshes, shadow mapping
- Fixed-timestep (120 Hz) physics loop
- Canvas 2D HUD overlay and Web Audio synthesized sound
