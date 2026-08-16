# ECHO VOID - Asset Pack

Assets extracted from the open-source Nine Chronicles client
(https://github.com/planetarium/NineChronicles), organized for use in a
non-commercial loading screen project called **ECHO VOID**.

## Contents

| Folder                | Contents                                                             |
|-----------------------|----------------------------------------------------------------------|
| `Characters/`         | 3 character spine sets with full animation references                |
| `Monsters/Regular/`   | 20 regular monster spine sets                                        |
| `Monsters/Bosses/`    | 10 boss monster spine sets                                           |
| `Maps/`               | 1 curated battle/dungeon background (PNG)                            |
| `Loading/`            | `loading.html` - the ECHO VOID branded loading screen (assets only)  |
| `ASSET_MANIFEST.json` | Machine-readable mapping of asset IDs to creative names and types    |

## Characters (3)

| ID          | Creative Name         | Original (Nine Chronicles)  |
|-------------|-----------------------|-----------------------------|
| `40100000`  | Valkyrie of the Void  | 발키리 (Valkyrie)            |
| `40100001`  | Dawn Lion             | 새벽의 사자 (Lion of Dawn)   |
| `40100002`  | Hela's Phantom        | 헬라의 환영 (Hela's Illusion)|

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

| ID        | Creative Name              | Original (Nine Chronicles)        |
|-----------|----------------------------|-----------------------------------|
| 202007    | Kitsune Chieftain          | 여우부족 대장 (Fox Tribe Chief)    |
| 203007    | Serimnir, Boar King        | 제림니르 (Serimnir)                |
| 205007    | Fenrir, Wind Devourer      | 펜리르 (Fenrir)                    |
| 206007    | Surtr, Flame Lord          | 수르트 (Surtr)                     |
| 207007    | Laufey, Frost Matriarch    | 라우페이 (Laufey)                  |
| 208007    | Jormungandr, World Serpent | 요르문간드 (Jormungandr)           |
| 209007    | Hera, Queen of Hel         | 헤라 (Hera)                        |
| 211000    | Surtr, Ashen Avatar        | 수르트 (Surtr)                     |
| 900001    | Fenrir, World Eater        | World Boss Fenrir                 |
| 900002    | Serimnir, Worldbreaker     | World Boss Serimnir               |

## Maps (1)

| File               | Description             |
|--------------------|-------------------------|
| `bg_dungeon_01.png`| Single curated dungeon background (1500x640) |

## Copyright & License Notice

**IMPORTANT - READ BEFORE USE**

This asset pack is a **derivative extraction** of design resources from
*Nine Chronicles*, developed by Planetarium and published at
https://github.com/planetarium/NineChronicles.

- The **source code** of Nine Chronicles is licensed under the
  **GNU AGPL-3.0**.
- The **design resources** (characters, monsters, backgrounds, icons, UI
  elements, animations) are **NOT** covered by the AGPL license. They are
  governed by the "Design Resources License" brand guideline published in
  the repository README, which permits:
  - **Non-commercial use** for derivative works that contribute to the
    expansion of the Nine Chronicles ecosystem.
  - **Commercial use is NOT permitted** in commercial works unrelated to
    the Nine Chronicles ecosystem.
  - Proper use is required; the resources must not be used in
    inappropriate content or in ways that could damage the brand's value.

### What this means for ECHO VOID

- These assets may be used **non-commercially** for a personal / fan /
  learning project that contributes to the Nine Chronicles ecosystem.
- They **must not** be used in a **commercial** game or product unrelated
  to the Nine Chronicles ecosystem.
- Keep this notice with the assets, and retain the attribution to
  Nine Chronicles / Planetarium.
- If you intend commercial use, you must obtain permission from the
  copyright holder (Planetarium) separately.

### Required attribution

When displaying or redistributing these assets, include:

> Nine Chronicles is (c) Planetarium. Design resources used under the
> Nine Chronicles Design Resources License (non-commercial use). For the
> full terms see https://github.com/planetarium/NineChronicles (README,
> "Design Resources License").

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
- Creative names are original to this pack for labeling; the underlying
  artwork and skeletons remain (c) Planetarium.

## Loading screen

`Loading/loading.html` is the **ECHO VOID** loading screen. It is an asset
showcase / loading UI built from the extracted atlases - it is not a game.
Open it in a browser (served from the project root so relative asset paths
resolve). It cycles through characters, regular monsters, bosses, and the
single dungeon map with an ECHO VOID boot animation.
