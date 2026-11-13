| [简体中文](../zh-Hans/installation.md) | [繁體中文](../zh-Hant/installation.md) | [English](../en/installation.md) |

| [主页](./home.md) | [内容索引](./index.md) | [安装指导](./installation.md) | [相关链接](./links.md) | [联系方式](./contact.md) | [许可证](./resource-packs-license.md) |

---

# 安装指导

## 安装资源包的方式

> 点击展开分类可以浏览具体步骤。

<details>
<summary>通过 Modrinth App 安装</summary>

1. 下载并安装最新版 Modrinth App。
2. 创建新的 Minecraft 实例，或选择与资源包兼容的已有实例。
3. 打开实例，进入 **Resource Packs（资源包）** 页面。
4. 使用以下任意一种方式安装资源包：
   - 点击 **Add Content（添加内容）**，搜索资源包并点击 **Install（安装）**。
   - 将下载好的 **.zip** 文件直接拖放到 **Resource Packs（资源包）** 页面。
5. 启动游戏实例。
6. 在游戏中进入 **选项 → 资源包**，将资源包移动到**已选资源包**，然后点击**完成**。
</details>

<details>
<summary>通过支持 Modrinth 检索的启动器安装</summary>

_前提：启动器内置 Modrinth 资源库检索功能，此处以 PCL2 为例。_

1. 打开 PCL2。
2. 在主页点击【下载】标签页。
3. 进入资源包分类。
4. 在搜索框输入该资源包的**英文名称**进行搜索。
5. 找到资源包，选择与您的 Minecraft 实例匹配的发布版本。
6. 下载；PCL2将自动把它安装至目标实例。
7. 启动游戏实例。
8. 在游戏中进入 **选项 → 资源包**，将资源包移动到**已选资源包**，然后点击**完成**。
</details>

<details>
<summary>手动安装</summary>

1. 下载资源包，并保持 **.zip** 格式。
2. 使用以下任意一种方式打开资源包文件夹：
   - 在游戏中进入**选项 → 资源包 → 打开资源包文件夹**
   - 或手动定位：

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

3. 将下载好的 **.zip** 文件复制或移动到 **resourcepacks** 文件夹。
4. 刷新资源包列表，若未显示请重新启动游戏。
5. 进入 **选项 → 资源包**，启用资源包。
</details>

### 注意事项

- 除非作者另有说明，否则请保持资源包为 **.zip** 格式。
- 多个资源包同时启用时，排列顺序越靠上优先级越高。
- 部分资源包需要额外安装前置项目才能获得完整视觉效果。

## 可能需要的前置项目

部分资源包，或其中的一些特定功能需要依赖前置项目实现，可能的原因通常如下：

- Minecraft 原生资源包能力有限，这类自定义功能不存在原版内置接口，需要前置模组 / 插件提供额外逻辑支持（例如 NBT、名称正则匹配、自定义渲染判定）。
- 该资源包基于指定前置资源包开发，缺少前置时，展示效果会不符合预期。
- 需要前置来写入、识别自定义 NBT 标记，作为材质 / 模型切换的判断依据。
- 部分交互行为、版本兼容补丁、性能优化逻辑由前置提供，原生资源包无法实现。
 
**必要前置项目会在各资源包详细页面中的「兼容性」条目说明，若没有特殊说明，则该资源包无需前置即可直接使用。**

以下会列举一些 Minecraft Java 版常用的、可实现资源包扩展功能的前置项目；在满足兼容条件时，列表内相同功能的前置项目可以互相替换使用。

<details>
<summary>项目列表</summary>

> **注意：该表格的内容不保证及时更新，也不保证完整性，仅供参考。**
> 若发现明显错误或过时内容，或有需要补充的具体内容，请于 Issues 页面指出。
> 为保证表格易于阅读，部分内容将使用英文缩写，相关细节详见下文缩写对照表。

| 前置名称 | 平台 | 功能说明 | 备注 |
| :---: | :---: | --- | --- |
| MCPatcher | 旧版原生客户端 | CIT、CTM 等扩展特性的原始实现 | 已停止维护，OptiFine 这类功能的起源，现已被 OptiFine 继承 |
| OptiFine（OF，高清修复）| Forge / 原生客户端 | 提供 CIT、CTM、CEM、CRE 等大量扩展特性，同时也支持光影渲染，实现 PBR | 老牌方案，新版本维护状态差，版本适配较复杂,和 Fabric 性能模组冲突 |
| OptiFabric | Fabric | 兼容层，让 OptiFine 在 Fabric 加载器运行 | 属于非官方兼容方案 |
| Sinytra Connector（信雅互联） | NeoForge/Forge | 兼容层，允许在 NeoForge/Forge 加载 Fabric 模组 | 本身不提供材质扩展能力，仅用于跨加载器运行 Fabric 生态的资源扩展模组 |
| Forgified Fabric API（FFAPI） | NeoForge/Forge | Fabric API 的 NeoForge 移植库 | 为 Fabric 模组在 NeoForge 上运行提供基础 API 依赖，常配合信雅互联使用 |
| Continuity | Fabric/NeoForge/Forge | 实现 CTM、方块 & 物品 ETT | 多用于 CTM 连接纹理类资源包 |
| Iris（光影加载器） | Fabric | 原生兼容绝大部分 OF 光影包，实现 PBR | 本身不提供 CIT/CTM/CEM 材质扩展；PBR 依赖它的渲染能力 |
| CIT Resewn（CITR） | Fabric | 实现 CIT | 已停止维护，兼容 OF 的 `.properties` 格式 CIT |
| CITResewnNeoPatcher | NeoForge | 补丁，让 CITR 通过信雅互联在 NeoForge 运行 | 依赖 CITR、信雅互联、FFAPI |
| CIT Resewn Continuation | Fabric/NeoForge | CITR 的非官方续作分支 | 原 CITR 停止维护后的主流接替方案 |
| CIT Reforged | NeoForge/Forge | CITR 的 Forge 移植分支 | 把 CIT 能力带到Forge生态 |
| Variants-CIT | Fabric | 提供一套新 CIT 格式，相比传统 CIT 减少冗余、性能更好 | 不兼容 OF 原生 CIT 格式；和 CITR 互相独立 |
| Chime | Fabric | 扩展原版谓词 Predicate，支持名称正则、NBT、维度等条件渲染 | 使用原版 predicate json，和 `.properties` 格式 CIT 不互通 |
| Entity Texture Features（ETF，实体纹理特性） | Fabric/NeoForge/Forge | 自定义实体材质、实体发光效果 | 常搭配 EMF 使用，替代 OF 的 CEM / CRE |
| Entity Model Features（EMF，实体模型特性） | Fabric/NeoForge/Forge | 自定义实体模型、实体动画 | 常搭配 ETF 使用，支持 `.jem` / `.jpm` 实体模型格式 |

另外，社区将 OptiFine 的各项功能拆解为多款独立轻量模组，以此规避它闭源、更新适配慢、模组兼容性差等痛点。在此感谢 LambdAurora 整理了一份专门的替代方案清单：https://optifine.alternatives.lambdaurora.dev/

<summary>缩写对照表</summary>

| 缩写 | 英文全称 | 中文 | 说明 |
| :---: | :---: | :---: | --- |
| CTM | Connected Textures Mod | 连接纹理 | 方块相邻时自动拼接纹理 |
| CIT | Custom Item Textures | 自定义物品纹理 | 按物品名称、附魔、NBT 等条件切换物品纹理 / 模型 |
| CIM | Custom Item Models | 自定义物品模型 | 非正式别称，一般特指 CIT 里的模型分支 |
| CRE | Custom Random Entities | 随机实体纹理 | 同一个生物切换多套纹理，可随机或按条件切换 |
| CEM | Custom Entity Models | 自定义实体模型 | 替换实体 3D 模型 |
| ETT | Emissive Textures | 自发光纹理 | 发光贴图，不需要 Minecraft 中的光源便可高亮，也不属于光源 |
| PBR | Physically Based Rendering | 物理渲染材质 | 法线、高光、视差等贴图，有 LabPBR/OldPBR（SeusPBR）两套主流 Minecraft PBR 纹理规范 |
| CCL | Custom Colors | 自定义颜色 | 自定义染色纹理、调色板 |
| CFM | Custom Fonts | 自定义字体 | 自定义宽高、特殊字符、HD 字体 |
| CWL | Custom World Layers | 自定义天空 | 自定义天空盒、云层、星空、日出日落 |
| CPM | Custom Panorama Modes | 自定义全景图 | 主菜单全景背景替换 |
| CPA | Custom Particles | 自定义粒子 | 替换粒子贴图、动画 |
</details>
</details>

---

| [主页](./home.md) | [内容索引](./index.md) | [安装指导](./installation.md) | [相关链接](./links.md) | [联系方式](./contact.md) | [许可证](./resource-packs-license.md) |