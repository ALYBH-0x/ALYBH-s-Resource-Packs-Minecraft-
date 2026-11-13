| [简体中文](../../zh-Hans/project-original/alybh-re-construction.md) | [繁體中文](../../zh-Hant/project-original/alybh-re-construction.md) | [English](../../en/project-original/alybh-re-construction.md) |

| [Back to Index](../index.md) |

---

# ALYBH-REconstruction

> A set of resource packs that retain vanilla color palettes while redrawing block and item textures.

<details>
<summary>Click to expand release pages</summary>

- Modrinth：https://modrinth.com/project/XXdgF0ix
- Planet Minecraft：https://www.planetminecraft.com/texture-pack/1-6-1-21-1-alybh-reconstruction/
- KLPBBS：https://klpbbs.com/thread-131760-1-1.html
</details>


## Overview

This resource pack keeps Minecraft’s original color scheme and redraws textures for blocks, items and more for a fresh visual style.

It includes addon subpacks: base textures, entity textures, 3D models, emissive maps, 512x parallax maps, shield-to-banner conversion textures and simplified PVP textures. Many of these can be freely combined.

These subpacks can also be used standalone when their respective requirements are met.

## Full List

> Unless noted otherwise, "supported versions" refer to Minecraft Java Edition.
>
> Subpack descriptions are translated here for easier page editing and reading.

**Main Resource Pack**: Main pack [ALYBH-REconstruction](https://modrinth.com/project/XXdgF0ix). It contains all components listed below:

| Name | Description | Minimum Supported Version |
| --- | --- | :---: |
| [Essential](https://modrinth.com/project/jENldH2N) | Core texture assets including blocks, items, GUI, particles, misc assets and armor. | 1.6+ |
| [Entity](https://modrinth.com/project/z03jsnwL) | Mob textures to complement the Essential pack. | 1.6+ |
| [Models](https://modrinth.com/project/BgAaemDA) | 3D models and matching textures for blocks and items. | 1.13+ |
| Emissive | OptiFine-based emissive textures. | 1.13+ |
| 512x Parallax Maps | labPBR-compliant parallax maps for enhanced visuals. | 1.13+ |

**Additional Optional Packs**: Extra packs you may install optionally.

| Name | Description | Minimum Supported Version |
| --- | --- | :---: |
| [Shield to Banner Pattern](https://modrinth.com/project/ZjjnSUaf) | Replaces shield patterns with matching banner patterns. | 1.8+ |
| [PVP-Lite](https://modrinth.com/project/UjVnPaxc) | Visual tweaks and optimizations for PvP. | 1.6+ |


## Compatibility

> Unless noted otherwise, "supported versions" refer to Minecraft Java Edition.
>
> Some packs may load outside the listed range (usually newer releases) but may have missing content; such cases are not officially supported.

| ID | Name | Supported Versions | Dependencies |
| --- | --- | :---: | --- |
| A | Essential | 1.6.1–1.21.1 | - |
| B | Entity | 1.6.1–1.21.1 | - |
| C | Models | 1.13–1.21.1 | - |
| D | Emissive | 1.13–1.21.1 | OptiFine or other mods with emissive texture support |
| E | 512x Parallax Maps | 1.13–1.21.1 | Shaders and mods supporting the labPBR standard |
| a | Shield to Banner Pattern | 1.8–1.21.1 | - |
| b | PVP-Lite | 1.6.1– | - |

<details>
<summary>Detailed Compatibility Between Packs</summary>

This table shows pairwise compatibility when all required dependencies are installed. Legend:
- ✅: No conflicts, works as intended
- ℹ️: Incomplete results due to missing assets; other packs are required for full effect
- ⚠️: File overlap may occur; try adjusting load order (smaller, specialized packs usually go higher)
- ❌: Conflicting assets cause broken or ineffective visuals, or the pack requires companion packs

> When row and column IDs match, the cell shows how that pack works with vanilla assets alone. This single-pack state does not apply when combining it with other packs in the table.

**This matrix only describes pairwise compatibility.** When loading multiple packs together, priority order for these statuses is: ❌ ＞ ⚠️ ＞ ✅ ＞ ℹ️, except for special exceptions listed below.

**Example:**
- Pairing 512x Parallax Maps (E) with Entity (B) gives ℹ️; E + Essential (A) and B + Essential (A) are both ✅. If all three are enabled together, the combined result is ✅.

**You may modify the internal files of these packs manually to alter compatibility.**

> This is a symmetric compatibility matrix; only the lower-left triangle is filled. Swapping rows and columns yields identical results.

| ID | A | B | C | D | E | a | b |
| --- | --- | --- | --- | --- | --- | --- | --- |
| A | ✅ |  |  |  |  |  |  |
| B | ✅ | ✅ |  |  |  |  |  |
| C | ⚠️ | ✅ | ✅ |  |  |  |  |
| D | ℹ️ | ℹ️ | ℹ️ | ❌ |  |  |  |
| E | ✅ | ℹ️ | ℹ️ | ℹ️ | ❌ |  |  |
| a | ⚠️ | ✅ | ✅ | ℹ️ | ℹ️ | ✅ |  |
| b | ⚠️ | ✅ | ❌ | ℹ️ | ℹ️ | ✅ | ✅ |

**Special Exceptions:**
- Emissive (D) + Essential (A) + Entity (B) = ✅. D includes emissive assets for both A and B. If paired with only one of them, the missing set of textures results in ℹ️.
- Emissive (D) also has emissive textures made for Models (C), but without Essential (A) and Entity (B), the state remains ℹ️. If all four are enabled, A and C together give ⚠️. With the intended load order C ＞ A, the four-pack combination becomes ✅.

**Notes:**
1. ℹ️ only applies when required companion packs are missing. Assets in D made for packs you are not using do not count as missing. So A + B + D stays ✅ even without C.
2. The full main set is A + B + C + D + E. Load priority inside this set is C ＞ A.

</details>

## Changelog

See the Modrinth release page.

## Gallery

WIP

## Trivia

- This pack series can be considered a remake of the [ALYBH Collection](./alybh.md).
- The magenta slime on the Essential cover is its mascot. The Entity pack cover is assembled by recoloring and collaging its own mob textures.
- One possible recipe for the rabbit banner on the Shield to Banner Pattern cover: White Base, PurpleFlowerCharge, Purple Saltire, Purple Base, White Base, Purple Bordure, White Bordure.

## License

CUSTOM LICENSE FOR ALYBH'S RESOURCE PACKS (MINECRAFT)

See the [License](../resource-packs-license.md) page for full terms.

> Prior to June 23, 2026 (GMT+8), this Work was distributed without an explicit license and was therefore considered All Rights Reserved (ARR). Effective June 23, 2026 (GMT+8), the Author relicensed this Work under this License, including previously released versions, unless otherwise stated. This change affects licensing only and does not indicate that any previously released version has been modified or republished.

---

| [Back to Index](../index.md) |