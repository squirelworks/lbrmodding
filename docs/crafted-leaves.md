# Crafted Leaves

Primary files:
- `gml_GlobalScript_Crafted_Leaf.gml`
- `gml_GlobalScript_Crafted_Leaf_Type.gml`
- `gml_GlobalScript_Crafted_Leaf_Upgrade.gml`
- Related: `crafting_wrapper.gml`, `get_craft_set.gml`, `save_craft_set.gml`

## Structure (from Crafted_Leaf constructor)

```gml
function Crafted_Leaf(arg0, arg1 = {}, arg2 = undefined) constructor
{
    name = __("Unknown");
    description = "";
    game_item_type = UnknownEnum.Value_1;
    sprite = spr_placeholder;
    type = arg0;
    fusion_cost = {};
    transformation_cost = {};
    max_level = 20;
    min_ascend_craft_level = 30;
    min_ascend_craft_ascend_level = 11;
    props_sorted = [];
    quality_base = irandom_range(0.01, 100);
    // ...
    data = {
        ascend_level: 1,
        color_id: "def",
        id: -1,
        level: 1,
        locked: false,
        props: {},
        quality_base: 0,
        quality: 0,
        rand: irandom_range(100, 999),
        reroll_props_count: 0,
        shards: {},
        tier: 1,
        type_key: self.type.key
    };
}
```

## Key Methods / Behaviors
- `init` — generates ID, sets quality, props, adds to inventory (`global.craft_leaves_inventory` or backpack)
- `add_shard` — adds shards to props with RNG (seeded by id, rerolls, etc.)
- Props system: sorted props, selected prop, shard counts, max shards
- Quality, rarity, ascend levels, tiers, colors
- Fusion and transformation costs

## Modding Relevance
- New leaf types can be added by defining new `Crafted_Leaf_Type` entries and integrating with inventory, props, and boss targeting logic.
- Props are the main vector for custom effects (e.g. bonuses against specific Umbral bosses).
- Quality / RNG systems are heavily seeded and cached.

See the full GML in the local Export for complete method list (set_props, set_prop_values, upgrades, etc.).
