# grad-proposal-manual

计算机毕业设计开题报告通用实操手册 —— 一个遵循 **Anthropic Agent Skills 开放规范** 的技能（Skill），可直接安装到 Claude Code、WorkBuddy 等支持该格式的工具，也可作为纯提示词复制给任意 AI（Gemini / ChatGPT / 通义等）使用。

> 覆盖 Web 系统、算法/人工智能、App/小程序、数据分析等计算机全科方向，**不绑定任何固定技术栈**。

## 它能做什么

把"写毕设开题报告"拆成 4 步可复制流程：

1. **定题目 + 技术栈** —— 提供 4 类题目的通用公式、技术栈 5 问清单，以及让 AI 帮你确认题目的提示词。
2. **生成知网检索关键词** —— 关键词拆分公式 + 可直接粘贴到 CNKI 高级检索的检索式提示词（精准/泛/外文）。
3. **逐模块生成开题内容（12 个模块）** —— 选题背景与意义、国内外研究现状、文献综述、研究内容、关键问题与难点、核心创新点、研究方法与手段、技术路线、可行性分析、实现方案、研究进度安排、预期成果，每模块一段可复制提示词。
4. **参考文献整理与全文自检** —— 引用规范 + 自检清单，避免"现状/综述重复""创新/难点混淆"等常见坑。

所有提示词中的 `{题目}` `{技术栈}` `{场景}` 等是占位符，替换成你自己的内容即可直接发给 AI。

## 目录结构

```
grad-proposal-manual/
├── SKILL.md              # 主指令文件（必需的 YAML 头 + 流程说明）
├── references/
│   └── modules.md        # 第 3 步 12 个开题模块的完整提示词
├── LICENSE               # MIT
└── README.md             # 本文件
```

## 安装

本技能符合 Anthropic Agent Skills 规范，目录名必须与 `SKILL.md` 里的 `name` 一致（`grad-proposal-manual`）。

### Claude Code
```bash
# 个人级（所有项目可用）
cp -r grad-proposal-manual ~/.claude/skills/

# 或项目级（仅当前仓库，提交进 git 共享给团队）
mkdir -p .claude/skills && cp -r grad-proposal-manual .claude/skills/
```

### WorkBuddy
```bash
cp -r grad-proposal-manual ~/.workbuddy-ai/skills/      # 个人级
# 或项目级：
mkdir -p .workbuddy-ai/skills && cp -r grad-proposal-manual .workbuddy-ai/skills/
```

### 其他支持 Agent Skills 的工具
把整个 `grad-proposal-manual/` 目录放进该工具约定的 `skills/` 目录即可；工具会在你说"帮我写毕设开题报告"时自动触发。

### 纯复制使用（无需安装）
直接打开 `SKILL.md` 和 `references/modules.md`，把对应模块的提示词段落复制粘贴到任意聊天 AI 即可，占位符替换成你的真实内容。

## 使用流程

1. 按 `SKILL.md` 第 1 步定好题目 + 技术栈。
2. 按第 2 步生成知网检索式，检索并分类留存 15-20 篇文献。
3. 准备好功能设计文档（模块划分/功能点/数据库表）后，按 `references/modules.md` 逐模块生成开题正文。
4. 按第 4 步整理参考文献、跑自检清单。

## 许可证

[MIT](LICENSE)
