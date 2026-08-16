# ECHO VOID - Asset Pack

Original procedural pixel-art assets generated for the **ECHO VOID**
project.

## Contents

| Folder                | Contents                                                             |
|-----------------------|----------------------------------------------------------------------|
| `Characters/`         | 3 character spine sets with full animation references                |
| `Monsters/Regular/`   | 20 regular monster spine sets                                        |
| `Monsters/Bosses/`    | 10 boss monster spine sets                                           |
| `Maps/`               | 1 curated battle/dungeon background (PNG)                            |
| `Loading/`            | `loading.html` - the ECHO VOID branded loading screen (assets only)  |
| `UI/`                 | UI textures, icons and module prefab references (see below)          |
| `ASSET_MANIFEST.json` | Machine-readable mapping of asset IDs to creative names and types    |

## UI Assets

UI assets are curated from the game's UI resources and reorganized by use.
All names in this folder are original to this pack (not the original file
names) so they can be dropped into your own game.

### UI/Textures (screens & elements)

| Subfolder     | Contents                                                                 |
|---------------|--------------------------------------------------------------------------|
| `_top_level`  | Core UI elements: boxes, frames, buttons, item frames, HP bars, mileage  |
| `Shop`        | Shop background and gold-dust package art (EN variants)                  |
| `Inventory`   | Item frames/backgrounds shared with shop screens                         |
| `Result`      | Battle result / victory decorations                                      |
| `Loading`     | Loading screens (world, arena, shop, world boss, ...)                    |
| `Arena`       | PvP backgrounds, emblems, vs screens                                     |
| `Intro`       | Logos and title loading background                                       |
| `WorldClear`  | World-clear background art                                               |
| `Event`       | Event banner / image art (EN variants)                                   |
| `Staking`     | Staking mob art                                                          |
| `Synopsis`    | Prologue / story illustration art                                        |
| `TitleFrames` | Title frame icons                                                        |
| `Tooltip`     | Navigation tooltip background                                            |

### UI/Icons

| Subfolder             | Count | Contents                                   |
|-----------------------|-------|--------------------------------------------|
| `Character`           | 32    | Character costume + monster icons          |
| `BigCharacter`        | 4     | Large boss artwork (bosses only)           |
| `Item`                | 228   | Curated item icons (premium grade 5+)      |
| `FungibleAssetValue`  | 62    | Currencies: NCG, Crystal, AP, Hourglass, runes |
| `Buff`                | 31    | Buff / debuff status icons                 |
| `Skill`               | 15    | Boss skill icons (Fenrir, Serimnir)        |
| `ElementalType`       | 5     | Normal / Fire / Water / Land / Wind        |
| `Navigation`          | 26    | Menu navigation icons                      |
| `System`              | 5     | Popup / system icons                       |
| `Mail`                | 9     | Mail category icons                        |

Item icons were curated from the full game set (983 icons) down to the
important premium items only: grade 5+ materials and monster parts,
legendary consumables, grade 6+ equipment, and core currencies. The full
list lives in `ASSET_MANIFEST.json` under `ui.icons.Item` (228 items).

### UI/Modules

Unity prefab references for the main game screens (Shop, Inventory,
ItemInformation, ShopShelf, EnhancementInventory, MaterialItemsGrid,
GrindModule, ...). These are Unity `.prefab` files kept as structural
reference for your own UI implementation.

## Characters (3)

| ID          | Creative Name         |
|-------------|-----------------------|
| `40100000`  | Valkyrie of the Void  |
| `40100001`  | Dawn Lion             |
| `40100002`  | Hela's Phantom        |

Each character folder contains: `<id>.png`, `<id>.atlas.txt`, `<id>.skel.bytes`,
Unity importer artifacts (`*_Atlas.asset`, `*_Material.mat`,
`*_SkeletonData.asset`), and `ReferenceAssets/` with the full animation
clip set (Attack, Idle, Run, Walk, Hit, Die, Win, Casting, CriticalAttack,
Touch, TurnOver, ...).

## Monsters (30)

### Regular Monsters (20)

| ID        | Creative Name         |
|-----------|-----------------------|
| 201000    | Yggdrasil Seed        |
| 201001    | Yggdrasil Sprout      |
| 201003    | Yggdrasil Bloom       |
| 201005    | Yggdrasil Seedling    |
| 201007    | Spore Shroom          |
| 201008    | Yggdrasil Thicket     |
| 202000    | Foxkin Grunt          |
| 202003    | Foxkin Warrior        |
| 203000    | Boarkin Grunt         |
| 203003    | Boarkin Warrior       |
| 204000    | Yggdrasil Sludge      |
| 204020    | Yggdrasil Sludge      |
| 205000    | Wind Squire           |
| 205004    | Gale Gazelle          |
| 206000    | Mottled Lizard        |
| 206003    | Lizard Brute          |
| 207001    | Troll Digger          |
| 208001    | Frost Boar            |
| 209001    | Ganglöt               |
| 210007    | World 9 Wraith        |

### Boss Monsters (10)

| ID        | Creative Name              |
|-----------|----------------------------|
| 202007    | Kitsune Chieftain          |
| 203007    | Serimnir, Boar King        |
| 205007    | Fenrir, Wind Devourer      |
| 206007    | Surtr, Flame Lord          |
| 207007    | Laufey, Frost Matriarch    |
| 208007    | Jormungandr, World Serpent |
| 209007    | Hera, Queen of Hel         |
| 211000    | Surtr, Ashen Avatar        |
| 900001    | Fenrir, World Eater        |
| 900002    | Serimnir, Worldbreaker     |

## Maps (1)

| File               | Description             |
|--------------------|-------------------------|
| `bg_dungeon_01.png`| Single curated dungeon background (1500x640) |

## Copyright & License Notice

**IMPORTANT - READ BEFORE USE**

This asset pack contains **original procedural pixel-art** generated from
scratch for the ECHO VOID project. The PNG artwork does not reproduce or
derive the artwork of any existing game and carries no third-party
copyright claim.

For the **Spine skeleton data** (`*.skel.bytes`) and **atlas layouts**
(`*.atlas.txt`):

- These are retained as functional animation data. If you intend to
  redistribute this pack as fully independent original work, you should
  regenerate the skeletons yourself or remove them and keep only the
  original artwork.

## File format notes

- Characters and monsters are **Spine** skeletons:
  - `*.png` = texture atlas image
  - `*.atlas.txt` = atlas layout
  - `*.skel.bytes` = binary skeleton (bones, slots, and all animation
    timelines: idle, run, walk, attack, hit, die, win, casting, critical,
    touch, turn over)
  - `*_SkeletonData.asset` / `*_Material.mat` / `*_Atlas.asset` are Unity
    importer artifacts kept for compatibility with Unity/Spine import.
  - `ReferenceAssets/` = Unity animation-clip references naming the
    animation states.
- Creative names and artwork are original to this pack.

## Loading screen

`Loading/loading.html` is the **ECHO VOID** loading screen. It is an asset
showcase / loading UI built from the extracted atlases - it is not a game.
Open it in a browser (served from the project root so relative asset paths
resolve). It cycles through characters, regular monsters, bosses, and the
single dungeon map with an ECHO VOID boot animation.
