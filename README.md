# Shadow Heist — 2D Top-Down RPG (Java)

A 2D top-down cyberpunk stealth-action RPG built from scratch in core Java using Swing, focusing on modular object-oriented architecture, custom tilemap collisions, and persistent game state.

---

## Overview
Set in a dystopian cyberpunk city controlled by a corrupt megacorporation, players control **Nyx**, an operative infiltrating corporate facilities to collect evidence while avoiding automated patrol guards:
- **Dynamic Camera & World Rendering:** Tilemap renderer loading multi-layer maps from CSV files exported via Tiled, with a smooth following camera centered on the player.
- **Combat & Hitbox System:** State-driven combat (Idle, Run, Attack) with custom AABB hitbox calculation for melee swings and enemy contact damage.
- **Enemy AI:** Autonomous patrol guards that actively detect player line-of-sight, transition into chase mode, and execute attacks.
- **Progress Persistence:** Complete save/load pipeline storing player stats, score, and level state directly into a local database.
- **HUD & Menus:** Interactive main menu, pause overlay, health bar, and real-time score tracking.

---

## Level Architecture
- **Level 0 (Hub):** Introductory staging zone used to enter different parts of the facility.
- **Levels 1, 2 & 3:** Labyrinthine layout levels with increasing enemy density, item placements (Crypto Chips, Health Orbs), and escape objectives.

---

## Tech Stack & Tools
- **Language:** Java (JDK 17+)
- **GUI Framework:** Java Swing / AWT (Graphics2D rendering pipeline)
- **Database:** SQLite / MySQL (via JDBC)
- **Map Editor:** Tiled (CSV layer matrix export)
- **Documentation:** Full UML diagrams and architecture breakdown in `Shadow_Heist_Documentatie_Finala.pdf`

---

## Project Structure
```text
├── assets/                  # Sprites, backgrounds, audio, and CSV tilemaps
│   ├── backgrounds/         # Main menu and scene textures
│   ├── maps/                # CSV layer exports from Tiled
│   └── sprites/             # Nyx, Guard animations, and HUD elements
├── lib/                     # JDBC and SQLite dependencies
├── src/                     # Core Java source code
│   ├── entities/            # Player, Enemy AI, and Collectibles
│   ├── state/               # Game state management (Menu, Playing, Pause)
│   ├── tile/                # Map rendering and tile collision logic
│   └── main/                # Game loop, panel, and window initialization
├── Shadow_Heist_Documentatie_Finala.pdf  # Technical documentation
└── README.md
