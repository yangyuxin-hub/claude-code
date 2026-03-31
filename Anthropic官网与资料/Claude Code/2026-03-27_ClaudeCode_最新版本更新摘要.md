# Claude Code 最新版本更新摘要

> 完整 CHANGELOG：https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md
> 最后更新：2026-03-27

---

## v2.1.84（最新）

- **Windows 支持**：新增 PowerShell 工具（opt-in preview）
- `TaskCreated` Hook：任务创建时触发，可用于自动化工作流
- `WorktreeCreate` Hook 支持 HTTP 类型
- 团队/企业管理员可通过 `allowedChannelPlugins` 控制插件权限
- 优化 prompt cache 显示格式（"1.5m" 替代 "1512.6k"）
- 修复 voice push-to-talk 字符泄漏问题

## v2.1.83

- `managed-settings.d/` 目录：支持策略碎片化配置（企业管理用）
- 新增 `CwdChanged` / `FileChanged` Hook 事件
- 新增 transcript 搜索（transcript 模式下按 `/`）
- 粘贴图片现在在光标处插入 `[Image #N]` 标记
- `initialPrompt` 前置参数：自动提交 agent 第一轮对话

## v2.1.81

- `--bare` 标志：用于脚本化 `-p` 调用，跳过 hooks/LSP

## v2.1.80

- statusline 脚本新增 `rate_limits` 字段（5小时/7天窗口）
- Slash command 支持 `effort` 前置参数
- `--channels`（研究预览）：MCP 服务器可主动推送消息

## v2.1.79

- `--console` 标志：使用 Anthropic Console API 认证
- `/config` 菜单新增"显示每轮耗时"开关

## v2.1.78

- `StopFailure` Hook：API 错误处理
- `${CLAUDE_PLUGIN_DATA}` 变量：插件持久化状态存储
- **安全修复**：修复沙箱依赖缺失时静默禁用的问题

## v2.1.77

- Opus 4.6 默认最大输出 token 提升至 64k（上限 128k）
- `/fork` 重命名为 `/branch`（旧命令仍可用）
- `--resume` 速度提升 45%，内存减少 100-150MB

## v2.1.76

- MCP elicitation 支持：结构化输入对话框
- `-n / --name` 标志：命名会话
- `worktree.sparsePaths`：大型 monorepo 稀疏检出

## v2.1.75

- Opus 4.6 默认启用 1M 上下文窗口（Max/Team/Enterprise 计划）
- `/color` 命令：自定义会话 prompt 栏颜色

## v2.1.74

- `/context` 命令新增可操作建议
- `autoMemoryDirectory` 设置：自定义内存存储目录
- **修复严重内存泄漏**：streaming API 响应缓冲区
