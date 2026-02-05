# Contributing to Runly Protocol 🚀

首先，感谢你考虑为 Runly Protocol 做出贡献！正是有了像你这样的开发者，我们才能共同定义 **AI Native SOP 的工业标准**。

在提交你的 PR 之前，请先阅读以下指南。

## 🛠 我们欢迎哪些贡献？

* **Core Engine**: 优化 `runly-cli` 或执行引擎的性能与稳定性。
* **DSL Specification**: 对 RSS-DSL 语法的改进建议或新节点类型（Node Types）的定义。
* **SDKs**: 开发或维护不同语言（TS, Python, Rust, etc.）的执行插件。
* **SOP Blueprints**: 贡献高质量的业务 AI 化 SOP 模板（放在 `/examples` 目录下）。
* **Documentation**: 修复文档错误、增加用例或翻译。

## 📬 提交流程

1. **Fork** 本仓库并创建你的特性分支 (`git checkout -b feature/AmazingFeature`)。
2. **Commit** 你的修改。请遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范（如 `feat: add new hitl node capability`）。
3. **Push** 到你的分支 (`git push origin feature/AmazingFeature`)。
4. 在 GitHub 上开启一个 **Pull Request**。

## 📜 代码规范 (Golang)

* 所有代码必须通过 `go fmt` 和 `go vet`。
* 核心逻辑必须包含对应的单元测试（Unit Tests）。
* 如果你修改了协议规范，请同步更新 `docs/` 目录下的文档。

## ⚖️ 行为准则

我们致力于提供一个无障碍、包容且健康的社区环境。请在参与过程中保持专业与尊重。

---

*Turn Expertise into Opus.*
