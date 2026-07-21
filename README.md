# 🎓 女大学生微信聊天模拟器 — Girl Chat Simulator

> 一个基于 AI Skill 的仿真社交模拟器，通过与有完整人设的同龄女大学生进行微信式对话，在安全环境中练习和异性的沟通技巧。

[![Agent Skills Standard](https://img.shields.io/badge/Agent_Skills-Standard-8A2BE2)](https://github.com/agent-skills/skills.sh)
[![Multi-Runtime](https://img.shields.io/badge/Runtime-Claude_Code_|_Codex_|_Cursor_|_OpenClaw-blue)](https://github.com/agent-skills/skills.sh)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📖 这是什么

作为一个20岁左右的男生，你是否遇到过这些困境：

- 加上女生微信后不知道第一句话说什么
- 聊着聊着对方就敷衍了，不知道哪里出了问题
- 想约她出来但怕被拒绝，不知道什么时机合适
- 吵架冷战后想破冰但不知道怎么开口

**这个项目不是"AI女友"**——它是一个**安全练习场**。通过和三个有完整人设、性格各异的女大学生角色进行微信式对话，你可以：

- 🎯 练习话题开启、延续和切换
- 💡 学习感知情绪和调整沟通策略
- 📈 通过好感度系统获得即时反馈
- 🔄 安全地犯错、观察后果、改进方法

---

## 👩 三个角色

| 角色 | 性格 | 聊天风格 | 难度 |
|------|------|---------|------|
| 🎀 **苏念** | INFJ · 温柔文静型 | 回复偏短但用心，爱用~和...，慢热细腻 | ⭐⭐⭐ |
| 🌟 **林小鹿** | ENFP · 活泼元气型 | 表情包轰炸，哈哈哈刷屏，热情自来熟 | ⭐⭐ |
| ❄️ **沈玥** | INTJ · 清冷御姐型 | 回复简洁克制，外冷内热，对低质量话题零容忍 | ⭐⭐⭐⭐ |

三个角色覆盖了「暖 → 热 → 冷」三条温度线，基本囊括了现实中常见的女生类型。

---

## 🚀 快速开始

### 安装

```bash
# 克隆仓库到 skills 目录
git clone https://github.com/YOUR_USERNAME/girl-chat-simulator.git

# 复制 skills 到对应 runtime 的 skills 目录：

# Claude Code
cp -r girl-chat-simulator/.claude/skills/girl-* ~/.claude/skills/

# Codex
cp -r girl-chat-simulator/.claude/skills/girl-* ~/.codex/skills/

# Cursor / OpenClaw / 其他 runtime
# 复制到对应 runtime 的 skills 目录即可
```

### 使用

在任意支持 Agent Skills 标准的 AI 工具中输入：

```
/girl-chat-general    # 通用入口，可切换角色
/girl-sunian          # 直接和苏念聊天
/girl-linxiaolu       # 直接和林小鹿聊天
/girl-shenyue         # 直接和沈玥聊天
/girl-scenarios       # 选择场景卡片（S01-S08）
```

---

## 💬 对话格式

每条消息开头会显示好感度条：

```
【好感度 ████░░░░░░ 38%】「有点好感」
```

### 好感度阶段

| 进度条 | 百分比 | 阶段 | 她的表现 |
|--------|--------|------|---------|
| █░░░░░░░░░ | 0-15% | 陌生人 | 礼貌疏离，回复简短 |
| ███░░░░░░░ | 16-35% | 略感好奇 | 开始回问，偶尔主动 |
| █████░░░░░ | 36-55% | 有点好感 | 分享日常，emoji增多 |
| ███████░░░ | 56-75% | 明显喜欢 | 主动找话题，关心你 |
| ████████░░ | 76-90% | 暧昧期 | 暗示，深夜聊天 |
| ██████████ | 91-100% | 可以告白 | 就差一层窗户纸 |

---

## 🎬 场景卡片（S01-S08）

输入 `/girl-scenarios` 后选择：

| 编号 | 场景 | 练习目标 |
|------|------|---------|
| S01 | 刚加微信，第一句话怎么说 | 破冰技巧 |
| S02 | 评论她的朋友圈后转私聊 | 自然切入话题 |
| S03 | 聊了一周，想约她出来 | 邀约分寸 |
| S04 | 她突然不回消息了 | 化解冷场 |
| S05 | 发现她和别的男生走得很近 | 处理竞争心态 |
| S06 | 她心情不好找你倾诉 | 提供情绪价值 |
| S07 | 暧昧期，差一步确认关系 | 告白时机判断 |
| S08 | 吵架冷战后如何破冰 | 冲突修复 |

---

## ⚠️ 失败机制

这个模拟器有真实的社交惩罚机制（仅语言层面，不拉黑不删除）：

| 你的行为 | 她的反应 |
|---------|---------|
| 连续3轮低质量话题 | 回复变成单字/表情包敷衍 |
| 越界发言（过早暧昧） | "呃...我先去洗个澡🛀" |
| 严重踩雷（不尊重） | "你这样说话让我不太舒服" |
| 长期不联系 | 好感度自然衰减15-25% |

---

## 🏗️ 项目结构

```
.claude/skills/
├── girl-chat-general/          # 通用聊天入口
│   ├── SKILL.md
│   └── references/research/    # 6份调研报告
├── girl-sunian/                # 苏念 - 温柔文静型
│   ├── SKILL.md
│   └── references/
├── girl-linxiaolu/             # 林小鹿 - 活泼元气型
│   ├── SKILL.md
│   └── references/
├── girl-shenyue/               # 沈玥 - 清冷御姐型
│   ├── SKILL.md
│   └── references/
└── girl-scenarios/             # 场景卡片合集
    └── SKILL.md
```

---

## 📚 调研基础

本项目基于女娲Skill方法论完成多维度调研：

1. **微信聊天语料** — 小红书/贴吧/虎扑/知乎真实聊天记录
2. **语言特征** — 叠词/语气词/emoji/缩写/表情包文化
3. **社交阶段** — Knapp阶梯模型+社会渗透理论+中国大学生适配
4. **校园文化** — 2024-2026流行梗/APP生态/恋爱观/消费习惯
5. **常见错误** — 男生聊天减分行为+女生典型反应
6. **性格原型** — INFJ/ENFP/INTJ心理学基础+本土化描述

---

## 🔧 自定义

每个角色的 SKILL.md 都可以直接编辑：

- 调整好感度起始值
- 修改加减分幅度
- 增加或修改雷区
- 自定义角色的兴趣爱好和背景故事

---

## ⚡ 技术说明

- 基于 [Agent Skills 标准](https://github.com/agent-skills/skills.sh) 构建
- 兼容 Claude Code、Codex、Cursor、OpenClaw 等所有支持该标准的 runtime
- 对话仅存储在本地，不上传任何服务器
- 角色设定明确标注为 AI 模拟角色

---

## 📄 License

MIT

---

## 🙏 致谢

- [女娲 · Skill造人术](https://github.com/alchaincyf/nuwa-skill) — 调研与Skill蒸馏框架
- [达尔文Skill](https://github.com/alchaincyf/darwin-skill) — 质量评估与优化
- 角色设计灵感来自 MBTI 性格类型学和真实大学生社交行为研究

---

> 💡 **提示**：这个工具的目的是帮你练习和提高。现实中每个女生都是独一无二的，不存在"攻略公式"。真诚、尊重、做自己，永远是沟通中最重要的。
