# AI 内容创作 · 个人 IP 项目

## 项目定位

围绕 **Anthropic 生态 + AI 应用开发**建立个人 IP。

**身份**：AI 应用开发学生，研究 agent 架构，Anthropic / Claude 深度用户。笔名：小羊肖恩。

**内容方向**：Claude 系列模型、Claude Code、Anthropic 产品理念、agent 架构、AI 应用开发实践。

**目标**：写出自己满意的内容，同时建立个人影响力（辅助求职——让潜在雇主看到你的技术视角和判断）。不以课程变现为目的。

**受众**：也在研究 AI / agent / Claude 的人，有技术背景或主动学习的人。可假设读者知道 Claude Code 是什么、agent 是什么。

---

## 本文件夹内容说明

`goals.md` 和 `strategy.md` 是当前目标与策略。`knowledge/` 是身份背景与写作风格参考。

---

## 文件结构约定

```
/
├── CLAUDE.md / goals.md / strategy.md
├── articles/              ← 所有文章（每篇独立文件夹）
│   ├── {文章标题}/
│   │   ├── {文章标题}.md
│   │   ├── outline.md
│   │   ├── prompts/00-cover.md, 01-xxx.md ...
│   │   ├── 00-cover.png（2.35:1 封面）
│   │   └── 01~NN.png（正文图 16:9）
│   └── xhs-images/        ← 小红书配图
├── videos/                ← 视频内容（按方向分区，暂未启动）
├── knowledge/             ← about-me / writing-style 等
├── cases/                 ← 落地案例文档
├── reflections/           ← 月度复盘
├── reference/             ← Anthropic 官网资料 / 核心观点
└── topics/                ← 选题素材（主存储在飞书，本地为备份）
    ├── ideas.md
    └── 素材库/
```

配图生成方式见父目录 `CLAUDE.md`（baoyu-danger-gemini-web，并行生成）。

## 写作辅助 Skill

写公众号长文时，使用 `khazix-writer` skill（卡兹克风格写作）。已安装，直接调用即可。

---

## 背景与策略

@knowledge/about-me.md
@knowledge/writing-style.md
@goals.md
@strategy.md

## 内容进度

@progress.md

## 选题素材库

**主存储：飞书多维表格**（跨设备、支持看板拖拽）
- 地址：https://m13v62vijcp.feishu.cn/base/Xg4wbrz8EaUzPlstdhYc0KUjnBg
- **选题库**：标题 / 写作角度 / 平台 / 分类 / 状态（🔥今天必写 / ⚡本周可写 / 📌积累备用 / ✅已发布）
- **素材库**：标题 / 链接 / 来源 / 分类 / 状态（📥待消化 / 💡已转选题 / ⏸暂时搁置）/ 我的判断

> 新增选题/素材时，优先写入飞书多维表格。可让 Claude 用 lark-cli 帮你填写。

@topics/ideas.md
