# Project Overview

## Local Workspace Layout
```
artifacts/
├── Export/
│   ├── Code/          # 1232 .gml files (decompiled GML)
│   ├── Assembly/      # matching .asm
│   ├── Sprites/        # ~1350 PNG sprites
│   ├── Strings/        # strings.txt
│   └── RoomsToPNG/
├── GwenTea/             # game dump (saves remaining after cleanup)
├── Envy Save/           # separate save dump
└── LBR Decompile/       # was Ghidra output (cleaned)
```

## Export Stats
- 1232 GML scripts
- 1232 ASM files
- ~1350 PNG sprites (achievements, artifacts, autoblowers, backgrounds, etc.)

## Key Entry Points
- `gml_GlobalScript_init_game_data.gml` / `init_globals.gml` / `init_game_vars.gml`
- `gml_Object_o_init_Create_0.gml`
- Area system: `init_areas.gml`, `Area.gml`, `Area_Type.gml`
- Resource system: `Resource.gml`, `init_resources.gml`
- Crafted leaves: `Crafted_Leaf.gml`, `Crafted_Leaf_Type.gml`, `Crafted_Leaf_Upgrade.gml`
- Prestige / Crunch: `prestige_exec.gml`, `init_prestige_levels.gml`, `can_auto_crunch.gml`

## Observed Runner
- GameMaker Studio runner 2.29.4.0
- Startup logic previously located around `FUN_14038e160` (command line, data.win path)
