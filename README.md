# InvestDesk

个人投资管理方案：以飞书多维表格为数据库与 Agent 中枢，以 Skill 作为结构化协议，自研系统补齐初始化配置与实时行情同步。

## 定位

InvestDesk 不是从零自建的投资 App，而是：

- **飞书多维表格**：数据库、应用界面与 Agent 中枢
- **InvestDesk Skills**：定义持仓、交易、灵感、备选规则的结构化数据协议
- **自研系统**：负责初始化、模板搭建、实时行情/净值同步
- **外部 AI 工具**（扣子 / Trae Work / Codex）：可复用同一套 Skills

## 核心原则

- 数据不散落在聊天里，统一沉淀到飞书多维表格
- 多维表格 Agent 是主要录入、检索、分析和提醒入口
- Skill 保证跨 Agent 与外部工具的结构化输出
- 不做券商软件已经很强的实时行情终端，只做"和我的持仓、灵感、备选规则有关"的投资上下文管理

## 架构

详见 [`docs/architecture.md`](docs/architecture.md)。

## 技术方向

轻量 worker/CLI 项目：`Node.js + TypeScript + Playwright + lark-cli`。

```text
src/
  cli/
  feishu/
  instruments/
  quotes/
  jobs/
```
