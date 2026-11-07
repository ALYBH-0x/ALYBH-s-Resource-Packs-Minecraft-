| [簡體中文](../../zh-Hans/project-original/alybh-re-construction.md) | [繁體中文](../../zh-Hant/project-original/alybh-re-construction.md) | [English](../../en/project-original/alybh-re-construction.md) |

| [返回至內容索引](../index.md) |

---

# ALYBH式重構（ALYBH-REconstruction）

> 一套保留原版配色、重繪方塊與物品紋理的資源包組合。

<details>
<summary>點擊展開發布頁面</summary>

- Modrinth：https://modrinth.com/project/XXdgF0ix
- Planet Minecraft：https://www.planetminecraft.com/texture-pack/1-6-1-21-1-alybh-reconstruction/
- KLPBBS：https://klpbbs.com/thread-131760-1-1.html
</details>


## 內容簡介

這款資源包沿用遊戲原版配色，重新繪製了方塊、物品等各類紋理，帶來不一樣的視覺感受。

其提供基礎紋理、生物紋理、3D 模型、發光貼圖、512x 視差貼圖及盾旗轉換紋理、PVP 簡化紋理等附加分包，部分支持自由搭配。

這些附加分包在滿足對應條件時，也可拆分出來單獨使用。

## 詳細列表

> 若無特殊說明，“支持版本” 均指《Minecraft》Java 版的版本範圍。
> 
> 爲便於頁面編輯和瀏覽，分包的譯文僅在此條目顯示。

**主資源包（Main Resource Pack）**：主資源包 [ALYBH-REconstruction](https://modrinth.com/project/XXdgF0ix)。包含以下所有內容：

| 項目名稱 | 項目內容 | 支持的最低版本 |
|----------|----------|----------------|
| [Essential（基礎包）](https://modrinth.com/project/jENldH2N) | 核心紋理資源，包含方塊、物品、GUI、粒子、雜項、盔甲等內容。 | 1.6+ |
| [Entity（實體紋理包）](https://modrinth.com/project/z03jsnwL) | 生物紋理，用於補充 Essential 資源包中的生物資源。 | 1.6+ |
| [Models（模型包）](https://modrinth.com/project/BgAaemDA) | 爲方塊與物品提供 3D 模型和對應的紋理。 | 1.13+ |
| Emissive（自發光紋理包） | 基於 OptiFine 的自發光紋理。 | 1.13+ |
| 512x Parallax Maps（512x 視差貼圖包） | 基於 labPBR 規範的視差貼圖，增強視覺效果。 | 1.13+ |

**附加資源包（Additional Packs）**：可選安裝的附加資源包。

| 項目名稱 | 項目內容 | 支持的最低版本 |
|----------|----------|----------------|
| [Shield to Banner Pattern（盾牌圖案轉換爲旗幟圖案）](https://modrinth.com/project/ZjjnSUaf) | 將盾牌圖案替換爲與旗幟一致的圖案。 | 1.8+ |
| [PVP-Lite（PvP用簡化包）](https://modrinth.com/project/UjVnPaxc) | 針對 PvP 的視覺效果優化與調整。 | 1.6+ |


## 兼容性

> 若無特殊說明，“支持版本” 均指《Minecraft》Java 版的版本範圍。
> 
> 部分資源包或許可在支持範圍外（一般爲更高版本）加載，但存在內容缺失等問題，不作爲受支持場景。

| 標識符號 | 項目名稱 | 支持版本 | 需要前置 |
|----|----|----|----|
| A | Essential | 1.6.1–1.21.1 | - |
| B | Entity | 1.6.1–1.21.1 | - |
| C | Models | 1.13–1.21.1 | - |
| D | Emissive | 1.13–1.21.1 | 高清修復（OptiFine）及其他支持自發光紋理的模組 |
| E | 512x Parallax Maps | 1.13–1.21.1 | 支持 labPBR 標準的模組與着色器 |
| a | Shield to Banner Pattern | 1.8–1.21.1 | - |
| b | PVP-Lite | 1.6.1– | - |

<details>
<summary>各資源包相互兼容性的細節</summary>

下表展示各資源包**在均已安裝所需前置的前提下**，單獨使用或兩兩搭配時的兼容情況，釋義如下：
- ✅：無資源衝突，效果符合預期；
- ℹ️：因資源缺失等因素無法完全達到預期效果，需要搭配其他資源包補足；
- ⚠️：存在資源文件互相佔用，可嘗試調整資源包加載優先級（一般而言，體積更小、功能更專一的分包優先級更高）；
- ❌：存在資源文件用途衝突導致效果不佳或失效，或是使用時必須依賴其他配套資源包。

> 若表格行、列標識符號相同，該單元格代表該資源包獨立搭配原版資源時的兼容狀態；當它和本表內其他資源包組合使用時，這一項獨立狀態不再參與判斷。

**該二維表格僅用於描述兩個資源包兩兩組合的兼容結果**。同時加載多個資源包時，這些情況的優先級爲 ❌ ＞ ⚠️ ＞ ✅ ＞ ℹ️ ，特殊說明的情況除外。

**示例：**
- 512x Parallax Maps（E）與 Entity（B）兩兩搭配結果爲 ℹ️；E 與 Essential（A）、B 與 Essential（A）兩兩搭配均爲 ✅。因此三者同時啓用時，整體兼容性結果爲 ✅。

**在實際使用時，可以通過增刪資源包的內部文件來更改不同資源包之間的兼容性。**

> 本表爲對稱兼容矩陣，僅填充左下三角區域；行、列互換後的結果與已填寫單元格一致。

| 標識符號 | A | B | C | D | E | a | b |
|----|----|----|----|----|----|----|----|
| A | ✅ |  |  |  |  |  |  |
| B | ✅ | ✅ |  |  |  |  |  |
| C | ⚠️ | ✅ | ✅ |  |  |  |  |
| D | ℹ️ | ℹ️ | ℹ️ | ❌ |  |  |  |
| E | ✅ | ℹ️ | ℹ️ | ℹ️ | ❌ |  |  |
| a | ⚠️ | ✅ | ✅ | ℹ️ | ℹ️ | ✅ |  |
| b | ⚠️ | ✅ | ❌ | ℹ️ | ℹ️ | ✅ | ✅ |

**特殊例外：**
- Emissive（D）＋ Essential（A）＋ Entity（B）的整體兼容性結果爲 ✅。這是因爲 Emissive 資源包同時爲後兩者製作了相關資源，只與其中一者搭配時，另外的部分會缺失對應紋理而致使兼容性結果爲 ℹ️。
- Emissive（D）同時也爲 Models（C）製作了適配的自發光紋理，但由於缺失 Essential（A）、Entity（B），兼容性仍然爲 ℹ️。四者同時啓用時，兼容性因 A 和 C 的組合，結果爲 ⚠️。預期的資源包優先級設計爲 C ＞ A，這個情況下，四者的兼容性結果爲 ✅。

**註釋：** 
1. ℹ️ 只衡量 “已啓用包的配套是否齊全”，D 中爲未啓用分包準備的內容不會被使用，不算缺失；故 A ＋ B ＋ D 不因缺少 C 而改變兼容結果爲 ℹ️。
2. 主資源包的配置的分包爲 A ＋ B ＋ C ＋ D ＋ E。其中的資源的增刪優先級爲 C ＞ A。

</details>

## 更新記錄

詳見於 Modrinth 的發佈頁面。

## 畫廊

WIP

## 花絮趣聞

- 該系列資源包基本可以視爲[「ALYBH」合集](./alybh.md) 的重置版。
- Essential 資源包封面上繪製的品紅色史萊姆是吉祥物；而 Entity 資源包的封面是由其中的實體紋理調色後拼貼而成的。
- 關於 Shield to Banner Pattern 資源包封面上的兔子旗幟圖案，其中一個可能的合成步驟爲：白色旗幟、紫色花朵盾徽、紫斜十字、底紫橫條、底白橫條、紫色方框邊、白色方框邊。

## 許可證

CUSTOM LICENSE FOR ALYBH'S RESOURCE PACKS (MINECRAFT)

詳情見[許可證](../resource-packs-license.md)頁面。

> _在 2026 年 6 月 23 日（GMT+8）之前，本作品發佈時未明確指定許可協議，因此默認適用“保留所有權利（All Rights Reserved，ARR）”。自 2026 年 6 月 23 日（GMT+8）起，除非另有說明，作者已將本作品（包括此前已發佈的版本）重新許可（relicense）爲適用本許可證。本次變更僅涉及許可協議，不應解釋爲任何此前發佈版本已被修改、重新發布或重新分發。_  

---

| [返回至內容索引](../index.md) |