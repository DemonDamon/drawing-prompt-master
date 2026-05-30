# Drawing Prompt Master (绘画提示词大师) 🎨

这是一个基于 Manus Skill 规范构建的绘画提示词专家库，专为 **Lovart.ai** 等支持多模态工作流的 AI 绘图平台优化。它不仅提供高质量的提示词模板，更核心的功能是通过**多轮交互**引导用户进行创意“冷启动”，并输出符合 **Text-to-Visual-Prompt Protocol** 的结构化导演级指令。

## 🌟 核心特性

- **Lovart.ai 智能体联动**: 引导用户配合使用 Lovart.ai 的“收集图片灵感”功能，通过真实参考图提升角色还原度。
- **结构化输出规约**: 采用严格的 `[主题与布局设想] -> [视觉模块详解] -> [风格与配色方案] -> [技术参数建议]` 结构，确保 AI 绘图模型准确解析复杂画面。
- **极简符号化写法**: 针对“全家福”等多角色同框场景，采用 `角色名 (特征1, 特征2)` 的极简写法，防止特征串位。
- **多轮交互引导**: 支持从模糊意向到具体指令的渐进式构思。

## 📂 仓库结构

```text
drawing-prompt-master/
├── SKILL.md              # Skill 核心指令，包含多轮交互与输出规约
├── references/
│   ├── ip_characters.md  # 热门 IP 角色特征参考库
│   └── style_library.md  # 绘画风格与视觉效果库
├── scripts/              # 自动化脚本工具
└── templates/            # 提示词模板资源
```

## 🛠 如何使用

### 在 Manus 中使用
1. 将本仓库内容加载为 Manus Skill。
2. 告诉 Manus 你的模糊想法（例如：“我想画一张包含 20 个动漫角色的全家福”）。
3. 按照 Manus 的引导，逐步确定构图和风格，并在 Lovart.ai 中准备好**角色参考图 (Reference Images)**。
4. 获取 Manus 输出的**结构化中文视觉描述**和**英文直出 Prompt**。
5. 将英文 Prompt 复制到 Lovart.ai 中生成图片。

### 交互示例
> **用户**: 我想画个火影忍者的图，但不知道画什么。
>
> **Manus**: 没问题！我们可以一起构思。首先，你希望画面是单人特写还是群像？另外，为了在 Lovart.ai 中获得最佳效果，建议你先使用它的**“收集图片灵感”**功能，找几张鸣人或佐助的官方设定图备用。你想尝试哪种风格？

## 🤝 贡献指南
欢迎提交 PR 来扩充 `references/` 下的角色库和风格库，让绘画创意更加丰富。

---
*基于 [awesome-nanobanana-pro-zh](https://github.com/DemonDamon/awesome-nanobanana-pro-zh) 升级而来。*
