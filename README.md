# Drawing Prompt Master (绘画提示词大师) 🎨

这是一个基于 Manus Skill 规范构建的绘画提示词专家库，专为 **Lovart.ai** 等支持多模态智能体工作流的 AI 绘图平台优化。核心解决的问题是：**多角色同框时 AI 容易"编造"角色特征**。

## 🌟 核心特性

| 特性 | 说明 |
|:---|:---|
| **智能体搜图指令** | 提示词开头直接命令 Lovart.ai 智能体搜索并下载角色官方设定图到本地，作为严格参考，杜绝 AI 凭空编造 |
| **结构化输出规约** | 采用 `[搜图指令] → [主题布局] → [视觉模块] → [风格配色] → [技术参数] → [英文直出Prompt]` 六段式模板 |
| **极简符号化写法** | 多角色场景使用 `角色名 (特征1, 特征2)` 格式，防止特征串位 |
| **多轮交互引导** | 支持从模糊意向到具体指令的渐进式冷启动构思 |

## 🔑 为什么需要"智能体搜图指令"？

当一张图包含 20+ 个动漫角色时，纯文字描述会导致 AI 模型"分散注意力"，后排小尺寸角色几乎全部被编造。**解决方案**是利用 Lovart.ai 本身作为智能体的能力，在提示词开头下达硬性指令：

> **先去搜索引擎查找每个角色的官方设定图 → 下载到本地上下文 → 以此为严格参考再进行绘制**

这样即使角色数量庞大，每个人的面部、服装、配色都能被精准还原。

## 📂 仓库结构

```text
drawing-prompt-master/
├── SKILL.md              # Skill 核心指令（含智能体搜图指令模板）
├── references/
│   ├── ip_characters.md  # 热门 IP 角色特征参考库
│   └── style_library.md  # 绘画风格与视觉效果库
├── scripts/              # 自动化脚本工具
└── templates/            # 提示词模板资源
```

## 🛠 如何使用

### 在 Manus 中使用
1. 将本仓库内容加载为 Manus Skill。
2. 告诉 Manus 你的模糊想法（例如："我想画一张包含 20 个动漫角色的全家福"）。
3. Manus 会通过多轮交互帮你确定构图和风格。
4. 获取包含 **[AGENT ACTION REQUIRED]** 搜图指令的完整提示词。
5. 将完整提示词复制到 Lovart.ai，智能体会自动执行搜图 → 下载 → 绘制的完整流程。

### 输出示例

```text
[AGENT ACTION REQUIRED]
Before drawing, search the web, download, and use official character design images for:
Gon Freecss, Killua Zoldyck, Naruto Uzumaki, Gojo Satoru...
Use these downloaded images as strict references to prevent hallucination.

[DRAWING PROMPT]
Epic anime crossover group photo, 40+ iconic characters on a white brick plaza...
Front center: Gon Freecss (spiky black hair, green jacket), Killua (white hair, purple shirt).
...
```

## 🤝 贡献指南
欢迎提交 PR 来扩充 `references/` 下的角色库和风格库，让绘画创意更加丰富。

---
*基于 [awesome-nanobanana-pro-zh](https://github.com/DemonDamon/awesome-nanobanana-pro-zh) 升级而来。*
