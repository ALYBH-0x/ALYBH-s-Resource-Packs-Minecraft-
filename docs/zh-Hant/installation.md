| [簡體中文](../zh-Hans/installation.md) | [繁體中文](../zh-Hant/installation.md) | [English](../en/installation.md) |

| [主頁](./home.md) | [內容索引](./index.md) | [安裝指導](./installation.md) | [相關鏈接](./links.md) | [聯繫方式](./contact.md) | [許可證](./resource-packs-license.md) |

---

# 安裝指導

## 安裝資源包的方式

> 點擊展開分類可以瀏覽具體步驟。

<details>
<summary>通過 Modrinth App 安裝</summary>

1. 下載並安裝最新版 Modrinth App。
2. 創建新的 Minecraft 實例，或選擇與資源包兼容的已有實例。
3. 打開實例，進入 **Resource Packs（資源包）** 頁面。
4. 使用以下任意一種方式安裝資源包：
   - 點擊 **Add Content（添加內容）**，搜索資源包並點擊 **Install（安裝）**。
   - 將下載好的 **.zip** 文件直接拖放到 **Resource Packs（資源包）** 頁面。
5. 啓動遊戲實例。
6. 在遊戲中進入 **選項 → 資源包**，將資源包移動到**已選資源包**，然後點擊**完成**。
</details>

<details>
<summary>通過支持 Modrinth 檢索的啓動器安裝</summary>

_前提：啓動器內置 Modrinth 資源庫檢索功能，此處以 PCL2 爲例。_

1. 打開 PCL2。
2. 在主頁點擊【下載】標籤頁。
3. 進入資源包分類。
4. 在搜索框輸入該資源包的**英文名稱**進行搜索。
5. 找到資源包，選擇與您的 Minecraft 實例匹配的發佈版本。
6. 下載；PCL2將自動把它安裝至目標實例。
7. 啓動遊戲實例。
8. 在遊戲中進入 **選項 → 資源包**，將資源包移動到**已選資源包**，然後點擊**完成**。
</details>

<details>
<summary>手動安裝</summary>

1. 下載資源包，並保持 **.zip** 格式。
2. 使用以下任意一種方式打開資源包文件夾：
   - 在遊戲中進入**選項 → 資源包 → 打開資源包文件夾**
   - 或手動定位：

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

3. 將下載好的 **.zip** 文件複製或移動到 **resourcepacks** 文件夾。
4. 刷新資源包列表，若未顯示請重新啓動遊戲。
5. 進入 **選項 → 資源包**，啓用資源包。
</details>

### 注意事項

- 除非作者另有說明，否則請保持資源包爲 **.zip** 格式。
- 多個資源包同時啓用時，排列順序越靠上優先級越高。
- 部分資源包需要額外安裝前置項目才能獲得完整視覺效果。

## 可能需要的前置項目

部分資源包，或其中的一些特定功能需要依賴前置項目實現，可能的原因通常如下：

- Minecraft 原生資源包能力有限，這類自定義功能不存在原版內置接口，需要前置模組 / 插件提供額外邏輯支持（例如 NBT、名稱正則匹配、自定義渲染判定）。
- 該資源包基於指定前置資源包開發，缺少前置時，展示效果會不符合預期。
- 需要前置來寫入、識別自定義 NBT 標記，作爲材質 / 模型切換的判斷依據。
- 部分交互行爲、版本兼容補丁、性能優化邏輯由前置提供，原生資源包無法實現。
 
**必要前置項目會在各資源包詳細頁面中的「兼容性」條目說明，若沒有特殊說明，則該資源包無需前置即可直接使用。**

以下會列舉一些 Minecraft Java 版常用的、可實現資源包擴展功能的前置項目；在滿足兼容條件時，列表內相同功能的前置項目可以互相替換使用。

<details>
<summary>項目列表</summary>

> **注意：該表格的內容不保證及時更新，也不保證完整性，僅供參考。**
> 若發現明顯錯誤或過時內容，或有需要補充的具體內容，請於 Issues 頁面指出。
> 爲保證表格易於閱讀，部分內容將使用英文縮寫，相關細節詳見下文縮寫對照表。

| 前置名稱 | 平臺 | 功能說明 | 備註 |
| :---: | :---: | --- | --- |
| MCPatcher | 舊版原生客戶端 | CIT、CTM 等擴展特性的原始實現 | 已停止維護，OptiFine 這類功能的起源，現已被 OptiFine 繼承 |
| OptiFine（OF，高清修復）| Forge / 原生客戶端 | 提供 CIT、CTM、CEM、CRE 等大量擴展特性，同時也支持光影渲染，實現 PBR | 老牌方案，新版本維護狀態差，版本適配較複雜,和 Fabric 性能模組衝突 |
| OptiFabric | Fabric | 兼容層，讓 OptiFine 在 Fabric 加載器運行 | 屬於非官方兼容方案 |
| Sinytra Connector（信雅互聯） | NeoForge/Forge | 兼容層，允許在 NeoForge/Forge 加載 Fabric 模組 | 本身不提供材質擴展能力，僅用於跨加載器運行 Fabric 生態的資源擴展模組 |
| Forgified Fabric API（FFAPI） | NeoForge/Forge | Fabric API 的 NeoForge 移植庫 | 爲 Fabric 模組在 NeoForge 上運行提供基礎 API 依賴，常配合信雅互聯使用 |
| Continuity | Fabric/NeoForge/Forge | 實現 CTM、方塊 & 物品 ETT | 多用於 CTM 連接紋理類資源包 |
| Iris（光影加載器） | Fabric | 原生兼容絕大部分 OF 光影包，實現 PBR | 本身不提供 CIT/CTM/CEM 材質擴展；PBR 依賴它的渲染能力 |
| CIT Resewn（CITR） | Fabric | 實現 CIT | 已停止維護，兼容 OF 的 `.properties` 格式 CIT |
| CITResewnNeoPatcher | NeoForge | 補丁，讓 CITR 通過信雅互聯在 NeoForge 運行 | 依賴 CITR、信雅互聯、FFAPI |
| CIT Resewn Continuation | Fabric/NeoForge | CITR 的非官方續作分支 | 原 CITR 停止維護後的主流接替方案 |
| CIT Reforged | NeoForge/Forge | CITR 的 Forge 移植分支 | 把 CIT 能力帶到Forge生態 |
| Variants-CIT | Fabric | 提供一套新 CIT 格式，相比傳統 CIT 減少冗餘、性能更好 | 不兼容 OF 原生 CIT 格式；和 CITR 互相獨立 |
| Chime | Fabric | 擴展原版謂詞 Predicate，支持名稱正則、NBT、維度等條件渲染 | 使用原版 predicate json，和 `.properties` 格式 CIT 不互通 |
| Entity Texture Features（ETF，實體紋理特性） | Fabric/NeoForge/Forge | 自定義實體材質、實體發光效果 | 常搭配 EMF 使用，替代 OF 的 CEM / CRE |
| Entity Model Features（EMF，實體模型特性） | Fabric/NeoForge/Forge | 自定義實體模型、實體動畫 | 常搭配 ETF 使用，支持 `.jem` / `.jpm` 實體模型格式 |

另外，社區將 OptiFine 的各項功能拆解爲多款獨立輕量模組，以此規避它閉源、更新適配慢、模組兼容性差等痛點。在此感謝 LambdAurora 整理了一份專門的替代方案清單：https://optifine.alternatives.lambdaurora.dev/

<summary>縮寫對照表</summary>

| 縮寫 | 英文全稱 | 中文 | 說明 |
| :---: | :---: | :---: | --- |
| CTM | Connected Textures Mod | 連接紋理 | 方塊相鄰時自動拼接紋理 |
| CIT | Custom Item Textures | 自定義物品紋理 | 按物品名稱、附魔、NBT 等條件切換物品紋理 / 模型 |
| CIM | Custom Item Models | 自定義物品模型 | 非正式別稱，一般特指 CIT 裏的模型分支 |
| CRE | Custom Random Entities | 隨機實體紋理 | 同一個生物切換多套紋理，可隨機或按條件切換 |
| CEM | Custom Entity Models | 自定義實體模型 | 替換實體 3D 模型 |
| ETT | Emissive Textures | 自發光紋理 | 發光貼圖，不需要 Minecraft 中的光源便可高亮，也不屬於光源 |
| PBR | Physically Based Rendering | 物理渲染材質 | 法線、高光、視差等貼圖，有 LabPBR/OldPBR（SeusPBR）兩套主流 Minecraft PBR 紋理規範 |
| CCL | Custom Colors | 自定義顏色 | 自定義染色紋理、調色板 |
| CFM | Custom Fonts | 自定義字體 | 自定義寬高、特殊字符、HD 字體 |
| CWL | Custom World Layers | 自定義天空 | 自定義天空盒、雲層、星空、日出日落 |
| CPM | Custom Panorama Modes | 自定義全景圖 | 主菜單全景背景替換 |
| CPA | Custom Particles | 自定義粒子 | 替換粒子貼圖、動畫 |
</details>
</details>

---

| [主頁](./home.md) | [內容索引](./index.md) | [安裝指導](./installation.md) | [相關鏈接](./links.md) | [聯繫方式](./contact.md) | [許可證](./resource-packs-license.md) |