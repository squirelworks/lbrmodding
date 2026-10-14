# Areas

Extracted from `gml_GlobalScript_init_areas.gml` via UTMT export.

Areas are defined in `global.areas` as `Area` constructors with index, name, description, resources, galaxy, section, background, enemies, costs, unlock conditions, etc.

## Area Names (partial / extracted)
- Home Garden
- Neighbors' Garden
- Mountain
- Space
- THE VOID
- The Abyss
- The Celestial Plane
- The Mythical Garden
- The Volcano
- The Abandoned Research Station
- The Hidden Sea
- Leafsink Harbor
- The Leaf Tower
- The Moon
- The Infernal Desert
- The Cursed Pyramid
- The Inner Cursed Pyramid
- Kokkaupunki
- Cursed Kokkaupunki
- The Dark Glade
- Black Leaf Hole
- Dicey Meadows
- Glinting Thicket
- Fish Pond
- Industrial Harbor
- Biotite Forest
- The Exalted Bridge
- The Ancient Sanctum
- Vilewood Cemetery
- The Lone Tree
- Spark Range
- Spark Bubble
- Spark Portal
- Energy Shrine
- Plasma Forest
- Blue Planet Edge
- Green Planet Edge
- Red Planet Edge
- Purple Planet Edge
- Black Planet Edge
- Terror Graveyard
- Energy Singularity
- Fire Fields Portal
- The Shadow Cavern
- The Coal Mine
- Mount Moltenfury
- The Fire Temple
- Flame Brazier
- The Fire Universe
- Soul Portal
- Spiral Walk
- The Cheese Pub
- ... and many more (galaxies, soul, energy, fire, cursed, etc.)

## Galaxies
From `init_galaxies.gml`:
- Leaf Galaxy
- Sacred Nebula
- Energy Belt
- Fire Fields
- (and further galaxies with obfuscation checks)

## Notes for Modding
- New areas can be added by extending `global.areas` and related systems (resources, enemies, shops, dialog sections).
- Unlock conditions often check previous areas, resources, or prestige level.
- Umbral-related content (e.g. Spiral Walk / Umbral Cluster) appears in later areas.
