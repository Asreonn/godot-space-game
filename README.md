# Godot Space Game

A top-down space mining and base-building prototype in Godot 4.6. Fly a small ship, cut asteroids apart with a mining laser, collect the ore they drop and build a modular base station.

> **Status:** Paused prototype from early 2026. About 5.8k lines of GDScript. The game folder name in `project.godot` is still the placeholder "deneme".

## Features

- **Ship movement:** acceleration and friction, aim follows the mouse, right-click boost, and recoil while the beam fires.
- **Mining laser:** hold-to-fire beam with heat (shown on a cursor indicator), damage ticks, impact effects and a hologram shader.
- **Asteroid field:** weighted spawning, asteroids break apart with explosion VFX and drop iron and gold.
- **Inventory:** drag-and-drop item rows, stack splitting, carry and drop handling, all built from a shared item database.
- **Modular base station:** grid build slots, a module registry, a placement preview and a build UI near the station, plus base health and a HUD tooltip.
- **Camera and background:** smooth follow camera with zoom, parallax star field with twinkle.
- **Smoke tests:** headless scenes in `tests/` for base health, the build preview and gameplay balance.

## Controls

| Input | Action |
|---|---|
| `WASD` / arrow keys | Move |
| Mouse | Aim |
| Left mouse | Fire the mining laser |
| Right mouse | Boost |
| `E` / `Q` or mouse wheel | Zoom in / out |

## Run

1. Install [Godot 4.6](https://godotengine.org/download) (GL Compatibility renderer).
2. Open `project.godot` in the editor and press **F5**.

Smoke tests can be run headless, e.g. `godot --headless --path . res://tests/base_health_smoke.tscn`.

## Layout

```
Scenes/   Player, Weapons, Environment, Base, Inventory, Items, UI, VFX, Camera
Shaders/  hologram.gdshader
Assets/   sprites (ship, asteroids, ore, stars)
tests/    smoke-test scenes
events.gd global signal bus (autoload)
```
