| [简体中文](../../zh-Hans/project-original/alybh-re-construction.md) | [繁體中文](../../zh-Hant/project-original/alybh-re-construction.md) | [English](../../en/project-original/alybh-re-construction.md) |

| [返回至内容索引](../index.md) |

---

# ALYBH式重构（ALYBH-REconstruction）

> 一套保留原版配色、重绘方块与物品纹理的资源包组合。

<details>
<summary>点击展开发布页面</summary>

- Modrinth：https://modrinth.com/project/XXdgF0ix
- Planet Minecraft：https://www.planetminecraft.com/texture-pack/1-6-1-21-1-alybh-reconstruction/
- KLPBBS：https://klpbbs.com/thread-131760-1-1.html
</details>


## 内容简介

这款资源包沿用游戏原版配色，重新绘制了方块、物品等各类纹理，带来不一样的视觉感受。

其提供基础纹理、生物纹理、3D 模型、发光贴图、512x 视差贴图及盾旗转换纹理、PVP 简化纹理等附加分包，部分支持自由搭配。

这些附加分包在满足对应条件时，也可拆分出来单独使用。

## 详细列表

> 若无特殊说明，“支持版本” 均指《Minecraft》Java 版的版本范围。
> 
> 为便于页面编辑和浏览，分包的译文仅在此条目显示。

**主资源包（Main Resource Pack）**：主资源包 [ALYBH-REconstruction](https://modrinth.com/project/XXdgF0ix)。包含以下所有内容：

| 项目名称 | 项目内容 | 支持的最低版本 |
|----------|----------|----------------|
| [Essential（基础包）](https://modrinth.com/project/jENldH2N) | 核心纹理资源，包含方块、物品、GUI、粒子、杂项、盔甲等内容。 | 1.6+ |
| [Entity（实体纹理包）](https://modrinth.com/project/z03jsnwL) | 生物纹理，用于补充 Essential 资源包中的生物资源。 | 1.6+ |
| [Models（模型包）](https://modrinth.com/project/BgAaemDA) | 为方块与物品提供 3D 模型和对应的纹理。 | 1.13+ |
| Emissive（自发光纹理包） | 基于 OptiFine 的自发光纹理。 | 1.13+ |
| 512x Parallax Maps（512x 视差贴图包） | 基于 labPBR 规范的视差贴图，增强视觉效果。 | 1.13+ |

**附加资源包（Additional Packs）**：可选安装的附加资源包。

| 项目名称 | 项目内容 | 支持的最低版本 |
|----------|----------|----------------|
| [Shield to Banner Pattern（盾牌图案转换为旗帜图案）](https://modrinth.com/project/ZjjnSUaf) | 将盾牌图案替换为与旗帜一致的图案。 | 1.8+ |
| [PVP-Lite（PvP用简化包）](https://modrinth.com/project/UjVnPaxc) | 针对 PvP 的视觉效果优化与调整。 | 1.6+ |


## 兼容性

> 若无特殊说明，“支持版本” 均指《Minecraft》Java 版的版本范围。
> 
> 部分资源包或许可在支持范围外（一般为更高版本）加载，但存在内容缺失等问题，不作为受支持场景。

| 标识符号 | 项目名称 | 支持版本 | 需要前置 |
|----|----|----|----|
| A | Essential | 1.6.1–1.21.1 | - |
| B | Entity | 1.6.1–1.21.1 | - |
| C | Models | 1.13–1.21.1 | - |
| D | Emissive | 1.13–1.21.1 | 高清修复（OptiFine）及其他支持自发光纹理的模组 |
| E | 512x Parallax Maps | 1.13–1.21.1 | 支持 labPBR 标准的模组与着色器 |
| a | Shield to Banner Pattern | 1.8–1.21.1 | - |
| b | PVP-Lite | 1.6.1– | - |

<details>
<summary>各资源包相互兼容性的细节</summary>

下表展示各资源包**在均已安装所需前置的前提下**，单独使用或两两搭配时的兼容情况，释义如下：
- ✅：无资源冲突，效果符合预期；
- ℹ️：因资源缺失等因素无法完全达到预期效果，需要搭配其他资源包补足；
- ⚠️：存在资源文件互相占用，可尝试调整资源包加载优先级（一般而言，体积更小、功能更专一的分包优先级更高）；
- ❌：存在资源文件用途冲突导致效果不佳或失效，或是使用时必须依赖其他配套资源包。

> 若表格行、列标识符号相同，该单元格代表该资源包独立搭配原版资源时的兼容状态；当它和本表内其他资源包组合使用时，这一项独立状态不再参与判断。

**该二维表格仅用于描述两个资源包两两组合的兼容结果**。同时加载多个资源包时，这些情况的优先级为 ❌ ＞ ⚠️ ＞ ✅ ＞ ℹ️ ，特殊说明的情况除外。

**示例：**
- 512x Parallax Maps（E）与 Entity（B）两两搭配结果为 ℹ️；E 与 Essential（A）、B 与 Essential（A）两两搭配均为 ✅。因此三者同时启用时，整体兼容性结果为 ✅。

**在实际使用时，可以通过增删资源包的内部文件来更改不同资源包之间的兼容性。**

> 本表为对称兼容矩阵，仅填充左下三角区域；行、列互换后的结果与已填写单元格一致。

| 标识符号 | A | B | C | D | E | a | b |
|----|----|----|----|----|----|----|----|
| A | ✅ |  |  |  |  |  |  |
| B | ✅ | ✅ |  |  |  |  |  |
| C | ⚠️ | ✅ | ✅ |  |  |  |  |
| D | ℹ️ | ℹ️ | ℹ️ | ❌ |  |  |  |
| E | ✅ | ℹ️ | ℹ️ | ℹ️ | ❌ |  |  |
| a | ⚠️ | ✅ | ✅ | ℹ️ | ℹ️ | ✅ |  |
| b | ⚠️ | ✅ | ❌ | ℹ️ | ℹ️ | ✅ | ✅ |

**特殊例外：**
- Emissive（D）＋ Essential（A）＋ Entity（B）的整体兼容性结果为 ✅。这是因为 Emissive 资源包同时为后两者制作了相关资源，只与其中一者搭配时，另外的部分会缺失对应纹理而致使兼容性结果为 ℹ️。
- Emissive（D）同时也为 Models（C）制作了适配的自发光纹理，但由于缺失 Essential（A）、Entity（B），兼容性仍然为 ℹ️。四者同时启用时，兼容性因 A 和 C 的组合，结果为 ⚠️。预期的资源包优先级设计为 C ＞ A，这个情况下，四者的兼容性结果为 ✅。

注释：** 
1. ℹ️ 只衡量 “已启用包的配套是否齐全”，D 中为未启用分包准备的内容不会被使用，不算缺失；故 A ＋ B ＋ D 不因缺少 C 而改变兼容结果为 ℹ️。
2. 主资源包的配置的分包为 A ＋ B ＋ C ＋ D ＋ E。其中的资源增删的优先级为 C ＞ A。

</details>

## 更新记录

详见于 Modrinth 的发布页面。

## 画廊

WIP

## 花絮趣闻

- 该系列资源包基本可以视为[「ALYBH」合集](./alybh.md) 的重置版。
- Essential 资源包封面上绘制的品红色史莱姆是吉祥物；而 Entity 资源包的封面是由其中的实体纹理调色后拼贴而成的。
- 关于 Shield to Banner Pattern 资源包封面上的兔子旗帜图案，其中一个可能的合成步骤为：白色旗帜、紫色花朵盾徽、紫斜十字、底紫横条、底白横条、紫色方框边、白色方框边。

## 许可证

CUSTOM LICENSE FOR ALYBH'S RESOURCE PACKS (MINECRAFT)

详情见[许可证](../resource-packs-license.md)页面。

> _在 2026 年 6 月 23 日（GMT+8）之前，本作品发布时未明确指定许可协议，因此默认适用“保留所有权利（All Rights Reserved，ARR）”。自 2026 年 6 月 23 日（GMT+8）起，除非另有说明，作者已将本作品（包括此前已发布的版本）重新许可（relicense）为适用本许可证。本次变更仅涉及许可协议，不应解释为任何此前发布版本已被修改、重新发布或重新分发。_  

---

| [返回至内容索引](../index.md) |