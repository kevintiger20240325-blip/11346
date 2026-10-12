---
description: 全局长期记忆：重要事实、约定与经验教训
tags: [memory, conventions, lessons]
created: "2026-10-12"
updated: "2026-10-12"
---

# 全局长期记忆

<!--
  WHAT: 给 Pi 的轻量长期记忆，记录值得以后回顾的重要事实。
  WHY: 让 Pi 不用每次会话重新发现稳定上下文。
  WHEN: 确认了重要事实、做出长期决定、或学到可复用的约束时更新。
-->

## 约定
- 全局 AGENTS.md 位于 `~/.pi/agent/AGENTS.md`，是跨项目的通用工作规范。
- 记忆层级：全局记忆优先于项目记忆（逻辑上全局 > 项目）；各级记忆内容均可随时修改。

## 环境
- macOS 系统 Python 受 PEP 668 保护，不能直接 `pip install`；第三方库装进独立 venv（如 `~/.pdf-venv` 已装 reportlab+pypdf，`~/.twitter-cli-venv` 装 twitter-cli）。
- 生成 PDF 用 `~/.pdf-venv/bin/python`，中文用系统 PingFang（reportlab TTFont 加载 /System/Library/Fonts/PingFang.ttc）。

## 经验教训
- HN 官方 Algolia API（hn.algolia.com/api/v1/search?tags=story&numericFilters=created_at_i>=...）可零登录按分数取任意时段热帖，是 X 不可用时的合法替代源。
- X/Twitter 无公开接口，twitter-cli 需要用户自己导出 auth_token+ct0；拒绝使用 GitHub 上泄露的他人凭据（硬底线）。
