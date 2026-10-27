<div align="center">

# ⚡ CYBER-NEXUS: OVERDRIVE — ULTRA EDITION

**A premium single-file neon arcade shoot-em-up. Zero dependencies. Zero build step. One HTML file.**

![Version](https://img.shields.io/badge/version-2.0--ULTRA-EA00D9?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNCIgaGVpZ2h0PSIxNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJ3aGl0ZSI+PHBhdGggZD0iTTEzIDJMMyAxNGg3bC0xIDhsMTAtMTJoLTdsMS04eiIvPjwvc3ZnPg==)
![License](https://img.shields.io/badge/license-MIT-00F0FF?style=for-the-badge)
![Size](https://img.shields.io/badge/game-200%20KB%20single%20file-F7B500?style=for-the-badge)
![Engine](https://img.shields.io/badge/engine-vanilla%20JS%20%2B%20Canvas-7CFF6B?style=for-the-badge)

**[▶ PLAY IN BROWSER — no install, no login](https://somersetnomad.github.io/cyber-nexus-overdrive/)**

*or download [`index.html`](index.html) and double-click it — works fully offline.*

</div>

---

<div align="center">
<img src="screenshots/01-title-screen.png" alt="CYBER-NEXUS: OVERDRIVE title screen" width="820">
</div>

Pilot the experimental **VX-9 VANGUARD** against the Bydo machine-swarm. Bend time with **Chrono-Dodge**, shatter space with **Quantum EMP**, unleash **OVERDRIVE**, and evolve your loadout through 26 augmentation modules across 4 rarity tiers. Three colossal titan-class bosses await — how deep into the Nexus can you push?

## 📸 Gallery

| | |
|---|---|
| <img src="screenshots/02-combat.png" alt="Wave 9 combat with bullet patterns and combo system" width="400"> | <img src="screenshots/03-titan-boss.png" alt="Cyber-Lord Prime titan boss encounter" width="400"> |
| *Wave 9 — bullet weave, combo x11, graze scoring* | *CYBER-LORD PRIME — armored core + weakpoint pods* |
| <img src="screenshots/04-upgrade-draft.png" alt="Upgrade draft with rarity cards" width="400"> | <img src="screenshots/05-wave-modifier.png" alt="Fortress Line wave modifier banner" width="400"> |
| *Level-up draft — 3 choices, reroll or skip for points* | *FORTRESS LINE — one of 4 wave modifiers* |
| <img src="screenshots/06-run-summary.png" alt="Signal Lost run summary screen" width="400"> | |
| *SIGNAL LOST — full run debrief with 9 tracked stats* | |

## 🎮 Controls

| Input | Action |
|---|---|
| `W A S D` / Arrow keys | Thrust |
| Mouse | Aim |
| `Space` / Hold Left Mouse | Fire |
| `E` / Right Mouse | **Quantum EMP** — shockwave that erases bullets & stuns |
| `Shift` (hold) | **Chrono-Dodge** — bullet-time; grazing builds EMP charge |
| `Q` | **OVERDRIVE** — temporary god-mode weapon evolution |
| `1` `2` `3` | Pick upgrade card |
| `P` | Pause · `M` — Audio |

📱 **Touch supported** — virtual joystick + fire/EMP/chrono buttons appear automatically on mobile.

## 🚀 What's in the ULTRA build

<details open>
<summary><b>Feature matrix (v1.0 jam build → v2.0 ULTRA)</b></summary>

| System | v1.0 | v2.0 ULTRA |
|---|---|---|
| Enemy types | 3 | **9 + elite (gold) variants** |
| Bosses | 1 | **3 multi-phase titans with weakpoints** |
| Upgrades | 6 | **26 across 4 rarities** (Common → Legendary) |
| Draft mechanics | — | **Reroll ×2 per run, skip-for-points** |
| Combo system | multiplier | **Rank ladder D → X with decaying meter** |
| Bullet time | — | **Chrono-Dodge + graze-charged EMP** |
| Ultimate | — | **Overdrive with charge economy** |
| Wave design | linear | **Budget director + 4 modifiers + formations** |
| Pickups | 1 | **5: Repair, Cell, Magnet, Pulsar, Cache** |
| Audio | beeps | **Procedural adaptive soundtrack (4 layers) + 20+ synth SFX** |
| Visual FX | trails | **Particle/shard/shockwave/floaters, parallax nebula, CRT & chromatic aberration filters** |
| Screens | 1 | **Menu, HUD, draft, salvage, pause, settings, game-over debrief** |
| Meta | score | **High score, deployments, total kills, best combo — persisted** |
| Platforms | desktop | **Desktop + full touch controls** |

</details>

<details>
<summary><b>Titan-class boss roster</b></summary>

| Titan | Signature mechanics |
|---|---|
| 🟡 **CYBER-LORD PRIME** | Rotating armor core, destructible weakpoint pods, enrage phase at low HP |
| 🟣 **VOID MAW DEVOURER** | Gravity wells that bend your bullets, teleport dashes, maw barrage |
| 🔴 **OMEGA SERAPH-9** | Rotating laser cross, telegraphed dash-slashes, flower-pattern bullet hell finale |

Every 5th wave is a titan engagement, followed by a **Salvage Protocol** reward screen.

</details>

<details>
<summary><b>26 augmentations across 4 rarities</b></summary>

| Common | Rare | Epic | Legendary |
|---|---|---|---|
| Damage Amp | Split Cannon | Homing Pods | Railgun Core |
| Overclock | Piercing Rounds | Orbital Drone | Twin Reactor |
| Hull Plating | Ricochet Shells | Tesla Coil | Phoenix Protocol |
| Barrier Matrix | Critical Matrix | Chrono Mastery | Overload Core |
| Thruster Tuning | Lethality Core | EMP Surge | Golden Rounds |
| Grav-Magnet | Nano Repair | Adrenal Boost | Temporal Aura |
| — | XP Circuitry | — | — |
| — | Vampire Rounds | — | — |

</details>

## 🛠️ Tech notes

- **Single self-contained `index.html`** (~200 KB, ~4,800 lines) — no framework, no bundler, no assets folder; all art is canvas-drawn, all audio is synthesized live via the Web Audio API
- Custom engine: fixed-timestep game loop with **hit-stop & slow-mo**, additive FX render pass, glow-sprite cache, spatial collision resolution
- Lookahead music scheduler (DynamicsCompressor master chain) with 4 intensity layers that react to wave state
- Persistence via `localStorage`; runs at 60 FPS on integrated graphics
- Works offline (the only external request is an optional Google Font, gracefully degraded)

## ▶️ Run it

**Option A — just open it:** download `index.html` and double-click.

**Option B — local server:**

```bash
git clone https://github.com/somersetnomad/cyber-nexus-overdrive.git
cd cyber-nexus-overdrive
python3 -m http.server 8080   # or: npx serve
# open http://localhost:8080
```

## 🌐 Host your own copy (GitHub Pages)

1. Fork or use this template
2. **Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save**
3. Your build goes live at `https://somersetnomad.github.io/cyber-nexus-overdrive/`

## 📜 Changelog

- **v2.0 — ULTRA EDITION** *(this build)* — 10× content expansion: 9 enemy types, 3 titan bosses, 26 upgrades, combo ranks, graze/EMP/Overdrive systems, procedural soundtrack, touch support, full visual overhaul
- **v1.0 — jam build** — original 3-enemy, single-boss prototype

## 📄 License

Released under the [MIT License](LICENSE) — fork it, remix it, ship it.
