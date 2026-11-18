# Souls-like

*[Version française](README.fr.md)*

A third-person action game inspired by the Souls series: explore a dungeon and an open world, fight patrolling knights and take on a boss.
Solo academic project made with **Unreal Engine 5.3** and **Blueprints** (February – March 2024).

## Features

- **Melee and ranged combat**: sword combo, bow, shield block and dodge roll. The player switches weapons during play, and an animation state machine handles each weapon's movement and attacks.
- **Patrolling enemies**: the Gold Knight is driven by a Behavior Tree and a Blackboard. It moves between patrol points, chases the player on sight and returns to patrol when it loses them.
- **Target lock** on an enemy, enemy health bars and hit feedback.
- **Boss** with a health bar, at least two attacks and an enrage phase.
- **Lantern puzzle**: lanterns must be lit in the right order to unlock a door; a wrong sequence resets the puzzle.
- **Interaction system**: a parent Blueprint shared by every interactive object, with an on-screen key prompt and a visual effect.
- **Inventory**: weapon pickups and healing potions, kept between levels.
- **Death sequence**: death animation, then a death screen to retry or return to the menu.
- **Three maps**: main menu, an indoor dungeon built with Cube Grid, and an outdoor world built with Landscape and Gaea, with props from Quixel Bridge.
- **UI**: health and resources, pause menu, interaction prompt.

## Project structure

| Folder | Contents |
| --- | --- |
| `Content/Blueprints/Character` | Player character, game mode, weapon enum |
| `Content/Blueprints/Boss` | Boss |
| `Content/Blueprints/Interaction` | Interaction parent class and lantern interaction |
| `Content/Assets/Enemy/GoldKnight/Blueprints` | Gold Knight: AI controller, Behavior Tree, Blackboard, health bar |
| `Content/Assets/Player_Character/Animations` | Animation Blueprint and montages (combo, block, roll, drink, shoot) |
| `Content/UI` | HUD, main menu, pause menu, death screen, interaction prompt |
| `Content/ThirdPerson/Maps` | `MainMenu`, `ThirdPersonMap` (dungeon), `OpenWorld` |

## Running the project

1. Install **Unreal Engine 5.3**.
2. Open `MidtermProject/MidtermProject.uproject`.
3. Open the `MainMenu` map and press Play.

<details>
<summary>Assignment requirements</summary>

| Requirement | Done |
| --- | --- |
| 3+ maps: main menu, indoor level (dungeon), outdoor level (open world) | ✓ |
| UI: player HP, resources, pause menu | ✓ |
| Patrolling enemy: moves between points, chases the player on sight, returns to patrol | ✓ |
| Lantern puzzle: door to unlock, interactive objects, correct order, reset on wrong sequence | ✓ |
| Boss: health display, enrage mechanic, at least 2 attacks | ✓ |
| Player death sequence: animation, transition to death screen, retry or return to menu | ✓ |
| Interaction system: interactive objects, visual effect, keyboard/gamepad key | ✓ |
| Inventory: weapon pickup, healing items, inventory kept | ✓ |
| Environment: Cube Grid indoors, Landscape and Gaea outdoors, Quixel Bridge props | ✓ |
| Combat system: melee combos, ranged attack, defensive action | ✓ |

</details>
