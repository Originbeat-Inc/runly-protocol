# Runly Protocol (RSS-DSL) 🚀

> **Turn Expertise into Opus.**
> **AI Native SOP 封装协议** —— 定义基于业务 AI 化场景的工业级标准。

[![Version](https://img.shields.io/badge/version-v1.0.0--rc-673DE7?style=flat-square)](https://github.com/runly-protocol/runly)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/status-AI--Native-00D4FF?style=flat-square)](#)

---

## 💡 什么是 Runly Protocol?

在 AI 时代，传统的流程图已无法承载非线性的智能决策。**Runly Protocol (RSS)** 是一套 **AI Native SOP 封装协议**。我们的目标不仅是赋能 AI 架构师与超级个体，更是为了**定义一套基于业务 AI 化场景的 SOP 工业标准**。

正如 Docker 封装了运行环境，Runly 封装了业务 AI 化的执行路径。通过 RSS-DSL (Domain Specific Language)，开发者可以将非标的“Prompt 交互”升级为具备强类型准入、异构模型路由、人工卡点（HITL）以及自动分账能力的**数字化逻辑资产**。

---

## ✨ 核心特性

* **AI Native 架构**: 原生适配 AI 执行特性，通过逻辑门限与强类型 Schema 根除 AI 幻觉，确保业务 100% 确定性。
* **业务资产化**: 将碎片化的业务逻辑封装为可确权、可分发的 `.runly` 文件，实现逻辑的资产化与标准化。
* **人机协同 (HITL)**: 原生支持流程挂起与 **Runly Me** 专家审批，实现复杂业务场景下的专家级闭环。
* **商业分账 (Commerce)**: 协议层内置结算逻辑，支持实时分账（Royalty Share），让逻辑调用即结算。
* **安全防篡改**: 集成 Ed25519 数字签名，确保资产在流转过程中逻辑完整，不可篡改。

---

## 🏗️ 核心架构 (The 4-Domain Model)

Runly 协议由四个互联的域组成，构成了业务 AI 化的标准框架：

| 领域 (Domain) | 职责说明 |
| :--- | :--- |
| **Manifest** | **协议名片**。定义 URN 唯一标识、版本确权与创作者身份。 |
| **Dictionary** | **数据字典**。定义变量强类型、外部 API 映射及可视化资产交付标准。 |
| **Topology** | **拓扑逻辑**。定义 AI 任务、逻辑门及人工审批（HITL）的状态机流转。 |
| **Commerce** | **商业分账**。定义定价模型、版税比例及自动结算契约。 |

---

## 🚀 快速上手

### 1. 安装 Runly CLI
```bash
# 下载并安装 Runly 工具链
curl -fsSL [https://get.runly.pro/install.sh](https://get.runly.pro/install.sh) | sh
```

### 2. 编写协议示例 (expert_logic.yaml)
```yaml
manifest:
  urn: "urn:runly:expert:market-analysis:v1"
  title: "AI 业务化选品分析"

dictionary:
  inputs:
    - name: "target_asin"
      type: "string"
      pattern: "^[A-Z0-9]{10}$"
      required: true

topology:
  nodes:
    - id: "ai_analysis"
      type: "AI_TASK"
      config: { prompt: "分析业务主体 {{inputs.target_asin}}..." }
      on_success: "expert_audit"
    - id: "expert_audit"
      type: "HITL"
      config: { instruction: "请基于 AI 分析结果完成最终业务授权" }

commerce:
  pricing: { amount: 0.85, currency: "USDT" }
  royalty: { creator_share: 0.80, platform_share: 0.20 }
```

###  3. 编译、签名并发布
```bash
# 验证并生成加密资产 .runly
runly-cli build expert_logic.yaml --key ./your_private.key

# 发布至 Runly Store
runly-cli publish expert_logic.runly
```

---
## 📡 报流协议标准 (RSS Message)

Runly 定义了统一的报文格式，确保 SDK、执行引擎与专家终端（Runly Me）之间的数据对齐：
```json
{
  "header": {
    "protocol_version": "v1.0",
    "trace_id": "req-8899-001",
    "timestamp": 1738746029
  },
  "asset": {
    "urn": "urn:runly:expert:market-analysis:v1",
    "signature": "ed25519:..."
  },
  "payload": {
    "current_node": "expert_audit",
    "status": "SUSPENDED",
    "state_data": { 
      "action": "RESUME", 
      "instruction": "..." 
    }
  }
}
```

---
##  🎨 视觉系统 (Visual Identity)

* Primary Color: #673DE7 (Electric Purple)

* Secondary Color: #00D4FF (Aurora Blue)

* Typography: Plus Jakarta Sans / Inter / JetBrains Mono

---
##  🤝 参与贡献
我们正在寻找对 业务 AI 化标准 感兴趣的贡献者。无论是优化 DSL 语法、开发多语言 SDK 还是贡献垂直行业的 SOP 模版，我们都虚位以待。

详情请参阅 [CONTRIBUTING.md](https://github.com/Originbeat-Inc/runly-protocol/blob/main/CONTRIBUTING.md)。

---
## 📄 开源协议
本项目采用 [MIT License](https://github.com/Originbeat-Inc/runly-protocol/blob/main/LICENSE) 开源。

