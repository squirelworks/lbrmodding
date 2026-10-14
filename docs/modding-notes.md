# Modding Notes

## Approach
1. Use UndertaleModTool on `data.win` to export GML / ASM / sprites / strings.
2. Study constructors and `init_*` functions (they build the data tables).
3. For native behavior, Ghidra the runner (GameMaker 2.x).
4. Saves are binary `save.dat` (can be decoded to JSON for inspection).

## Adding Content
- **New leaf type**: Extend `Crafted_Leaf_Type`, define props, integrate into inventory and relevant bosses.
- **New area**: Add entry in `init_areas`, link galaxy/section/resources/enemies, set unlock conditions.
- **New crunch layer**: Mirror prestige system (`prestige_exec`, levels, rewards, shop resets). Need to hook resource multipliers, offline progress, and UI.
- **Boss-targeted props**: Crafted leaf props system is the natural place; look at how existing props apply bonuses and extend for Umbral bosses (Omnipresence, etc.).

## Observations
- Heavy use of global structs and constructors.
- Unlock / obfuscation functions are common (`is_obfuscated`, `check`, resource/area gates).
- RNG is often seeded from leaf ID + counters for reproducibility.
- Many systems have both "lite" and full info caches.
- Sprite and string exports are complete enough for UI recreation or reference.

## Cleanup
Large binaries (`data.win` ~50MB, Ghidra `.c`/`.gzf` ~60MB, runner, summary images) were removed to save space after documentation extraction. Re-dump if deeper native analysis is needed.

## Related Community Tools
- Save editors (e.g. Redcrafter/lbr-save-editor and forks)
- AutoHotkey automation scripts (various repos)
- Wiki: leafblowerrevolution.wiki.gg

Not affiliated with the official game.
