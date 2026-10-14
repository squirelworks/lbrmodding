# Key Systems

## Resources
- Defined in `Resource.gml` and `init_resources.gml`
- Helpers: `add_resources.gml`, `get_resource.gml`, `resource_is_unlocked.gml`, `build_resource_cost.gml`
- Used everywhere: areas, shops, crafting, prestige rewards

## Leaves
- Base: `Leaf.gml` (simple visual/step constructor)
- Variants: `Comm_Leaf.gml`, `Unique_Leaf.gml`, community leaves, resource leaves
- Blow / spawn logic: `blow_leaf.gml`, `spawn_comm_leaf.gml`, `check_spawn_comm_leaf.gml`
- Leafscenders: `Leafscender.gml`, `check_leafscenders.gml`

## Prestige / Crunch
- `prestige_exec.gml`
- `init_prestige_levels.gml`
- `can_auto_crunch.gml`
- `get_offline_crunches.gml`
- `get_prestige_resources.gml`
- Shop integration: `init_shop_prestige.gml`, `check_shop_prestige_level.gml`

## Areas & Enemies
- `Area.gml`, `Area_Type.gml`, `init_areas.gml`, `init_area_types.gml`
- `init_enemies.gml`, `get_random_available_boss_area.gml`, `get_boss_reward_terror.gml`
- Change area: `change_area.gml`

## Crafting / Shops
- `crafting_wrapper.gml`, `gui_item_crafting.gml`
- `Shop_Item.gml`, `build_shop_item.gml`, `init_shop_*.gml` (many shop variants)

## Other Notable Init Scripts
- Achievements, Artifacts, Banks, Cards, Challenges, Chests, Dice, Equipment, Events, Galaxies, Mines, Recipes, Dialogs, etc.

Most systems are data-driven via the `init_*` functions that populate global structs. This makes adding content relatively straightforward once the constructors and unlock conditions are understood.
