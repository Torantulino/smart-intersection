<div align="center">

# 🚦 Smart Intersection

### Spacetime Traffic Controller

[![Play Now](https://img.shields.io/badge/%E2%96%B6_PLAY_NOW-blue?style=for-the-badge&logo=github&logoColor=white)](https://torantulino.github.io/smart-intersection/)

[![Built with AutoGPT AutoPilot](https://img.shields.io/badge/built_with-AutoGPT_AutoPilot-7c3aed?style=flat-square)](https://agpt.co)
[![Zero Dependencies](https://img.shields.io/badge/dependencies-zero-2dd4bf?style=flat-square)](.)
[![Build Time](https://img.shields.io/badge/build_time-single_conversation-f59e0b?style=flat-square)](.)

---

*What if intersections didn't have traffic lights — but had brains?*

</div>

## The Story

This entire simulation was designed, coded, and deployed in a single conversation with an AI. No frameworks. No build step. No dependencies. Just one HTML file and a concept:

**An intersection that thinks.**

Cars approach a shared crossroads from two perpendicular 2-way roads. Instead of stopping at a red light, each car *requests a spacetime window of safe passage* from a Smart Intersection controller. The controller — like an air traffic control tower — calculates a velocity that guarantees collision-free transit and commands the car to follow it.

No car ever stops completely. No car ever collides. The intersection orchestrates everything.

## How It Works

Cars cruise at random speeds along two looping 2-way roads that cross at one intersection. When a car enters the approach zone (~220px out), it contacts the **SmartIntersection** manager:

1. **Request**: "I'll arrive at time T, crossing at speed S — is it safe?"
2. **Negotiate**: The controller checks existing reservations from the perpendicular road
3. **Assign**: If clear → approved at full speed. If conflict → a new velocity is calculated to slot into a safe gap
4. **Execute**: The car smoothly adjusts to the assigned velocity and glides through

The result is a mesmerizing dance of vehicles weaving through each other without a single traffic light.

## What's Inside

- **Spacetime reservation system** — cars book time-slots through the intersection zone
- **Smooth car-following model** — prevents rear-end collisions on same-lane traffic
- **2-way looping roads** — with U-turn endpoints forming continuous circuits
- **Canvas 2D rendering** — 60fps with trail effects, glow, particles, and brake lights
- **Real-time HUD** — throughput, negotiation count, and average delay stats
- **Interactive controls** — add/remove cars, pause, keyboard shortcuts (H/V/R/Space)
- **Mobile support** — tap left half to add horizontal car, right half for vertical

## Run Locally

```bash
git clone https://github.com/Torantulino/smart-intersection.git
cd smart-intersection
open index.html
```

That's it. One file. Zero setup.

## Controls

| Key | Action |
|-----|--------|
| `H` | Add horizontal car |
| `V` | Add vertical car |
| `R` | Remove a car |
| `Space` | Pause/resume |
| Touch left/right | Add H/V car (mobile) |

## License

MIT — do whatever you want with it.

---

<div align="center">

Made with ✨ by **AutoGPT AutoPilot** × **Torantulino**

*No traffic lights were harmed in the making of this simulation.*

</div>
