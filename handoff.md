# everything-claude-code 交接文档（Handoff）
> 更新日期：2026-07-27 · 由 Claude Code 自动生成

## 一、这个项目是什么

- 第三方开源仓库的本地克隆（fork）：Anthropic 黑客马拉松获奖者 affaan-m 的 **Everything Claude Code（ECC）**，14 万+ star 的 AI agent harness 优化系统。
- 内容是一整套可安装的 Claude Code 插件资源：`agents/`（38 个子代理）、`skills/`（156 个技能）、`commands/`（72 个斜杠命令）、`hooks/`（会话持久化等自动化）、`rules/`、`mcp-configs/`，同时兼容 Codex、Cursor、OpenCode、Gemini 等 harness。
- 技术栈：Node.js >= 18，纯 CommonJS（无 TypeScript、无转译），ESLint + markdownlint，测试用自带的 `node tests/run-all.js`。
- 本地用途：作为参考/学习资料克隆到本机（2026-05-26 克隆），origin 是本人 fork，upstream 指向原作者仓库。

## 二、如何使用

- 主要是「读」：从 `README.md`（英文，另有 `README.zh-CN.md` 中文版）和 `CLAUDE.md` 入手了解结构；`COMMANDS-QUICK-REF.md` 是命令速查。
- 若要跑测试：
  ```bash
  node tests/run-all.js
  ```
- 若要把其中的 agent/skill/hook 用到自己的 Claude Code：按上游 README 的安装指引操作（支持 plugin marketplace 安装），或手工复制单个 markdown/JSON 到自己的 `~/.claude/`。
- 版本参考：本地 `CHANGELOG.md` 最新为 1.10.0（2026-04-05），含 ECC 2.0 alpha（`ecc2/` 控制面二进制）。

## 三、遗留问题 / 未解决的问题

- 本地克隆停留在 2026-05-26 的状态；上游（affaan-m/ECC）非常活跃，本地大概率已落后上游大量提交。是否落后、落后多少**待确认**（本次未执行 fetch）。需要最新内容时先 `git fetch upstream` 再对比。
- 本地无任何自有修改（工作区干净），因此不存在合并冲突风险；同步策略（是否跟进上游、是否维护自己的定制分支）尚未决定。
- 未在本地跑过其测试与安装流程，可用性**待确认**。

## 四、远程仓库信息

- remote：
  - `origin` = `https://github.com/jzhu29git/everything-claude-code.git`（本人 fork）
  - `upstream` = `https://github.com/affaan-m/ECC.git`（原作者）
- 当前分支：`main`，与 `origin/main` 同步（无 ahead/behind），工作区干净（0 个未提交文件）。
- 最近提交：
  - `8bdf88e5` Merge pull request #1501 from affaan-m/feat/ecc2-board-observability-integration
  - `7992f8fc` feat: integrate ecc2 board observability prototype
  - `1a50145d` Merge pull request #1462 from affaan-m/fix/remove-legacy-ecc-install-refs
