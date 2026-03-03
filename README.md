# AI 自动化获客、留存与资产管理平台

本项目为 **GenAI for Business Challenge** 课程作业，面向资产管理公司（Private Wealth / Asset Management）设计了一个端到端 AI 工作台，用于支持客户从线索获取、开户引导到投后管理的全流程。

该平台以单页交互界面（HTML + Tailwind + Chart.js）展示，核心聚焦三类业务目标：
- 自动化获客（Lead Generation）
- 客户留存与持续互动（Engagement & Retention）
- 投资组合管理与顾问增效（Portfolio Management & Advisor Copilot）

## 1. 平台概览

平台以左侧导航组织 4 个核心页面模块：
- `Onboarding`：客户入职与资料采集进度管理
- `Engage`：实时信号抓取、客户意图识别、AI 冷启动邮件生成
- `Manage`：资产配置、风险预警、组合分析与 AI 问答
- `Profile`：客户 360 画像与人工审核输入区

## 2. 核心功能说明

### 2.1 Onboarding（入职管理）
- 展示活跃开户会话（示例：`ALL (60)`、`NEEDS ATTENTION (7)`）
- 跟踪客户资料完成度与资产规模（如进度条、完成步骤、AUM）
- 提供顾问当日任务看板（文档审核、跟进电话等）
- 集成 AI Assistant 快捷动作（如 `Compose email`、`Prepare call`）
- 展示潜在 LinkedIn 线索列表，支持批量查看

### 2.2 Profile（客户画像）
- 展示客户基础信息、注册时间、总流动资产
- 呈现 AI 已核验数据（证件、存款、风险偏好）
- 保留“人工必填”投资策略输入区，强调 Human-in-the-loop
- 将 AI 预处理与人工顾问判断进行分层衔接

### 2.3 Engage（智能触达与线索激活）
- 模拟多源实时抓取流（LinkedIn、新闻、个人网站、社媒）
- 一键同步至数据库（`SYNCHRONIZE TO DATABASE`）
- 自动生成潜在需求优先级（Liquidity Event / Diversification / Market Outlook）
- 输出系统简报（Prospectus Briefing）
- 生成个性化 Cold Email 草稿，并支持“人工审核后发送”
- 发送后写入 CRM（toast 提示：`Initial contact logged in CRM`）

### 2.4 Manage（投后管理与顾问 Copilot）
- 展示客户财务目标完成度（如可持续投资目标、资本保值）
- 风险告警（示例：Apple 持仓 12.1% 超过 10% 阈值）
- 组合可视化（Chart.js 环形图：Equities / FI / Alternatives / Cash）
- 明细分配与短期变化跟踪（1W Change）
- AI Workspace Assistant 对话：支持快捷问题与自由输入
- 自动生成组合总结，提示收益驱动与风险偏离项

## 3. 业务流程（端到端）

1. **获客**：从外部渠道抓取行为信号，识别高潜客户。
2. **建档与入职**：在 Onboarding / Profile 完成信息核验与风险画像。
3. **智能触达**：AI 生成个性化邮件草稿，顾问审核后发送。
4. **留存与经营**：在 Manage 页面持续监控组合、风险与客户目标达成。
5. **顾问增效**：通过 AI Assistant 减少信息整合和报告撰写成本。

## 4. 项目价值（Business Value）

- **效率提升**：自动完成信息聚合、初步分析与文案草拟
- **转化提升**：基于行为信号做个性化沟通，提高触达成功率
- **风险可控**：在客户组合层面实时提示集中度与偏离阈值问题
- **服务标准化**：将“获客-开户-管理”流程在统一工作台闭环

## 5. 技术实现（当前作业版本）

- 前端：`HTML + TailwindCSS + Vanilla JavaScript`
- 图表：`Chart.js`
- 交互方式：前端模拟（按钮触发、状态切换、示例数据）
- 页面切换：`switchPage('onboarding' | 'engage' | 'manage' | 'profile')`

> 注：当前版本为课程演示原型，AI 推理、数据库同步、CRM 写入与抓取流为界面级模拟，便于展示完整业务流程。

## 6. 后续可扩展方向

- 接入真实 CRM 与客户主数据（Salesforce / HubSpot / 内部系统）
- 用 LLM + RAG 实现可追溯投顾问答与报告自动生成
- 接入实时市场数据与风控规则引擎（集中度、波动、敞口）
- 建立合规审计链（消息留痕、审批记录、可解释性输出）
- 增加 KPI 看板（线索转化率、触达响应率、AUM 增长、留存率）

---

如需，我可以继续基于这份 README 再产出：
- 课程汇报版（更偏商业叙事）
- 面试作品集版（更偏技术架构）
- 英文版 README（可直接用于国际课程提交）
