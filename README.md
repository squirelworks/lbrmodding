# Leaf Blower Revolution Modding (lbrmodding)

Personal reverse-engineering and modding project for **Leaf Blower Revolution** (GameMaker Studio game).

## Goals
- Add new leaf types
- Implement a new crunch / prestige layer
- Crafted-leaf properties targeting unbeaten Umbral bosses (e.g. Omnipresence)

## Tools Used
- **UndertaleModTool (UTMT)** — parse `data.win`, export GML scripts, assembly, sprites, strings
- **Ghidra** — decompile the native GameMaker runner (`game.exe`)
- Save analysis (`save.dat` / decoded `save.json`)

## Project Structure (local exports)
- `Export/Code/` — 1232 decompiled `.gml` GlobalScripts + objects
- `Export/Assembly/` — matching `.asm`
- `Export/Sprites/` — ~1350 PNG sprites
- `Export/Strings/strings.txt` — string table
- Game dumps (data.win, runner) and Ghidra output were cleaned up for space

## Documentation
See the `docs/` folder for extracted notes, area lists, key systems (Crafted Leaves, Areas, Galaxies, Prestige/Crunch), and modding observations.

## Notes
- Game data lives in `data.win` (FORM/GEN8).
- Runner version observed: GameMaker 2.29.4.0.
- Most game logic is in GML GlobalScripts (especially `init_*`, resource/leaf/area systems).
- Crafted leaves are a rich system with props, shards, quality, ascend levels, etc.

This repository is for documenting findings and sharing modding knowledge. Not affiliated with the game developers.
