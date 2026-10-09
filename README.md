# AfterCare AI

基于 Deep Agents 的企业级智能售后分析与处理平台。

AfterCare AI 是一个面向电商售后运营场景的个人开源实践项目，重点展示 Python 后端、业务建模、AI Agent、权限审批、可观测性和评测能力。项目坚持先构建可验证的业务系统，再逐步引入 Agent；不以堆叠框架代替真实工程能力。

## 当前状态

- 版本阶段：V0.1
- 当前工作：需求设计与项目初始化
- 已实现功能：暂无业务功能
- 下一项任务：Day 1——售后业务需求分析、业务流程设计和 MySQL 核心实体建模

真实进度和验证记录以 [`docs/PROGRESS.md`](docs/PROGRESS.md) 为准。

## 规划中的核心能力

- 查询订单、商品、售后工单和退款记录
- 调查复杂售后问题并输出可核对的证据链
- 分析投诉、商品和供应商关联数据
- 检索售后政策并判断适用条件
- 对退款等敏感操作生成建议并进入人工审批
- 持久化和恢复 Agent 任务，记录工具调用与执行状态
- 对比单 Agent 与多 Agent 的效果、延迟、Token 和成本

以上均为目标能力，尚未实现。

## 文档导航

- [项目定位](docs/PROJECT.md)
- [产品需求](docs/PRD.md)
- [架构设计](docs/ARCHITECTURE.md)
- [数据库设计](docs/DATABASE.md)
- [开发路线图](docs/ROADMAP.md)
- [当前进度](docs/PROGRESS.md)
- [技术决策记录](docs/DECISIONS.md)
- [AI 协作规范](AGENTS.md)

## 目录概览

```text
backend/       Python 后端与 Agent 服务（待初始化）
frontend/      Web 前端（待初始化）
evaluations/   Agent 评测数据与工具（待设计）
data/seed/     可复现的模拟业务数据（待创建）
docs/          项目、需求、架构和进度文档
```

## 目标技术栈

初步规划使用 FastAPI、Pydantic、SQLAlchemy 2、Alembic、MySQL 8、Deep Agents、LangGraph、LangChain、Redis、Next.js 和 Pytest。版本、接入顺序及部分组件是否采用仍待分阶段验证；初始化阶段没有安装这些依赖。

## 开发原则

- 每次只完成一个可验证的增量。
- 用后端规则、最小权限和人工审批保护敏感操作。
- Agent 的结论必须关联证据，推断不得冒充事实。
- 所有“已完成”状态都必须有对应验证记录。

