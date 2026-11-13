| [简体中文](../zh-Hans/installation.md) | [繁體中文](../zh-Hant/installation.md) | [English](../en/installation.md) |

| [Home](./home.md) | [Index](./index.md) | [Installation](./installation.md) | [Links](./links.md) | [Contact](./contact.md) | [License](./resource-packs-license.md) |

---

# Installation

## Installation Instructions For Resource Packs

> Expand the section to view detailed steps.

<details>
<summary>Install via Modrinth App</summary>

1. Install the latest version of the Modrinth App.
2. Create a new Minecraft instance or select an existing one compatible with the resource pack.
3. Open the instance and navigate to **Resource Packs**.
4. Install the resource pack by either:
   - Clicking **Add Content**, searching for the resource pack, and selecting **Install**.
   - Dragging the downloaded **.zip** file directly into the Resource Packs page.
5. Launch the instance.
6. In Minecraft, open **Options → Resource Packs**, move the resource pack to **Selected**, then click **Done**.
</details>

<details>
<summary>Install via supported launchers with Modrinth search</summary>

_Requirement: The launcher supports built-in Modrinth resource library retrieval. PCL2 is used as example here._

1. Open PCL2.
2. Click the Download tab on the main page.
3. Enter the Resource Packs category.
4. Search the **English name** of this resource pack in the search box.
5. Locate the resource pack, select the release version matching your Minecraft instance.
6. Download it; PCL2 will automatically install it into the target instance.
7. Launch the instance.
8. In Minecraft, open **Options → Resource Packs**, move the resource pack to **Selected**, then click **Done**.
</details>

<details>
<summary>Install manually</summary>

1. Download the resource pack and keep it in **.zip** format.
2. Open the resource pack folder by either:
   - In-game **Options → Resource Packs → Open Pack Folder**
   - Or manually locating:

   **Windows**
   ```text
   %AppData%\.minecraft\resourcepacks
   ```

   **macOS**
   ```text
   ~/Library/Application Support/minecraft/resourcepacks
   ```

   **Linux**
   ```text
   ~/.minecraft/resourcepacks
   ```

3. Copy the downloaded **.zip** file into the **resourcepacks** folder.
4. Refresh the resource pack list or restart Minecraft if necessary.
5. Enable the resource pack via **Options → Resource Packs**.
</details>

### Notes

- Keep the resource pack as a **.zip** file unless instructed otherwise.
- Resource packs higher in the list take priority over those below.
- Some resource packs require additional mods or shaders for the intended visual effects.

## Potential Required Dependencies

Some resource packs, or certain features within them, require dependencies to function. Common reasons are listed below:

- Vanilla Minecraft resource packs have limited capabilities. These custom features do not have built-in vanilla interfaces and require additional logic provided by dependency mods/plugins (e.g., NBT, name regex matching, custom rendering predicates).
- The resource pack is developed based on a specified dependency resource pack; without it, the displayed effects will not work as expected.
- A dependency is required to write and read custom NBT tags, which serve as conditions for texture/model switching.
- Certain interactive behaviors, version compatibility patches, and performance optimization logic are implemented by dependencies and cannot be achieved by vanilla resource packs alone.

**Mandatory dependencies are specified in the "Compatibility" section on each resource pack's detail page. If no special note is given, the resource pack can be used directly without any dependencies.**

Below is a list of commonly used extensions for Minecraft Java Edition that add resource pack capabilities. Where compatibility permits, different dependencies implementing the same feature may be used interchangeably.

<details>
<summary>Project List</summary>

> **Notice: This table is not guaranteed to be up-to-date or complete and is for reference only.**
> If you spot obvious errors, outdated entries, or content that should be added, please open an issue on the Issues page.
> For readability, some entries use English abbreviations; refer to the abbreviation table below for details.

| Dependency Name | Platform | Description | Notes |
| :---: | :---: | --- | --- |
| MCPatcher | Old native client | Original implementation of extended features such as CIT and CTM | Discontinued. The origin of features later adopted by OptiFine |
| OptiFine (OF) | Forge / Native client | Provides many extended features including CIT, CTM, CEM, CRE, and supports shaders and PBR | Legacy solution. Poor maintenance for new versions, complex version support, conflicts with Fabric performance mods |
| OptiFabric | Fabric | Compatibility layer to run OptiFine on the Fabric loader | Unofficial compatibility solution |
| Sinytra Connector | NeoForge/Forge | Compatibility layer allowing Fabric mods to run on NeoForge/Forge | Does not add texture extensions by itself; only enables cross-loader Fabric resource extension mods |
| Forgified Fabric API (FFAPI) | NeoForge/Forge | NeoForge port of Fabric API | Provides base API dependencies for Fabric mods running on NeoForge/Forge, commonly used alongside Sinytra Connector |
| Continuity | Fabric/NeoForge/Forge | Implements CTM, block & item ETT | Primarily used for CTM connected-texture resource packs |
| Iris (Shader Loader) | Fabric | Natively supports most OF shader packs and enables PBR | Does **not** provide CIT/CTM/CEM texture extensions; PBR relies on its rendering pipeline |
| CIT Resewn (CITR) | Fabric | Implements CIT | Discontinued; supports OptiFine `.properties` CIT format |
| CITResewnNeoPatcher | NeoForge | Patch for running CITR via Sinytra Connector on NeoForge | Depends on CITR, Sinytra Connector and FFAPI |
| CIT Resewn Continuation | Fabric/NeoForge | Unofficial continuation fork of CITR | Main successor after original CITR was discontinued |
| CIT Reforged | NeoForge/Forge | Forge port fork of CITR | Brings CIT functionality to the Forge ecosystem |
| Variants-CIT | Fabric | Introduces a new CIT format with less redundancy and better performance than traditional CIT | Incompatible with native OF CIT format; independent from CITR |
| Chime | Fabric | Extends vanilla predicates, supports conditional rendering based on name regex, NBT, dimension, etc. | Uses vanilla predicate JSON; not interoperable with `.properties` CIT |
| Entity Texture Features (ETF) | Fabric/NeoForge/Forge | Custom entity textures, entity emissive effects | Often paired with EMF as a replacement for OF CEM / CRE |
| Entity Model Features (EMF) | Fabric/NeoForge/Forge | Custom entity models and entity animations | Often paired with ETF; supports `.jem` / `.jpm` entity model formats |

Additionally, the community has split OptiFine's features into separate lightweight mods to avoid its drawbacks: closed-source licensing, slow updates and poor mod compatibility. Special thanks to LambdAurora for maintaining a dedicated alternative list: https://optifine.alternatives.lambdaurora.dev/

<summary>Abbreviation Table</summary>

| Abbreviation | Full Name | Chinese | Description |
| :---: | :---: | :---: | --- |
| CTM | Connected Textures Mod | 连接纹理 | Automatically joins block textures when adjacent blocks match |
| CIT | Custom Item Textures | 自定义物品纹理 | Swap item textures/models based on item name, enchantments, NBT and other conditions |
| CIM | Custom Item Models | 自定义物品模型 | Informal alias, usually referring to model-based branches of CIT |
| CRE | Custom Random Entities | 随机实体纹理 | Assign multiple textures to the same entity, randomly or conditionally |
| CEM | Custom Entity Models | 自定义实体模型 | Replace entity 3D models |
| ETT | Emissive Textures | 自发光纹理 | Glowing texture maps that do not require in-game light sources and are not light sources themselves |
| PBR | Physically Based Rendering | 物理渲染材质 | Normal, specular, parallax and other maps; two major Minecraft PBR standards: LabPBR / OldPBR (SeusPBR) |
| CCL | Custom Colors | 自定义颜色 | Recolorable textures and custom palettes |
| CFM | Custom Fonts | 自定义字体 | Custom character dimensions, special glyphs, HD fonts |
| CWL | Custom World Layers | 自定义天空 | Custom skyboxes, clouds, starfields, sunrise/sunset |
| CPM | Custom Panorama Modes | 自定义全景图 | Replace main menu panorama background |
| CPA | Custom Particles | 自定义粒子 | Replace particle textures and animations |
</details>
</details>

---

| [Home](./home.md) | [Index](./index.md) | [Installation](./installation.md) | [Links](./links.md) | [Contact](./contact.md) | [License](./resource-packs-license.md) |