# Andy 的 Claude Code 核心操作指令

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/AIPMAndy/andy-claude-directives?style=social)](https://github.com/AIPMAndy/andy-claude-directives/stargazers)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

一套综合的 Claude Code 行为指南，结合了基础认知公理、马斯克的工程方法论和 Karpathy 的编码原则，旨在最大化执行质量并最小化常见的 LLM 错误。

**[English](./README.md) | [中文](./README_CN.md)**

## 这是什么

这是一个 **CLAUDE.md** 配置文件，旨在让 Claude Code：
- 从第一性原理思考，而非表面类比
- 在实现前质疑需求
- 编写最小化、外科手术式的代码变更
- 系统性验证结果
- 透明地处理不确定性

它建立在三大支柱之上：
1. **9 条认知公理**（熵增定律、还原论、概率不确定性等）
2. **马斯克 5 步工程法**（质疑 → 删除 → 简化 → 加速 → 自动化）
3. **Karpathy 4 大编码原则**（思考先于编码、简洁优先、外科手术式修改、目标驱动执行）

## 适用人群

**适合你使用，如果你：**
- 希望 Claude 更系统地思考，减少错误
- 需要透明的推理和明确的不确定性处理
- 重视最小化、精准的代码变更，而非"改进"
- 需要目标驱动的执行和可验证的检查点
- 在数据完整性至关重要的项目上工作

**这不是：**
- 项目模板（无脚手架、无 CI/CD、无技术栈）
- 应用框架
- 领域特定指令的替代品

## 如何使用

### 方式 1：直接使用
复制 [`CLAUDE.md`](./CLAUDE.md) 到你的项目根目录。Claude Code 会自动加载它。

### 方式 2：与现有 CLAUDE.md 合并
如果你已经有 `CLAUDE.md`，添加相关部分：
- 复制"核心操作指令"部分到顶部作为高层指导
- 如果需要系统性推理，合并"认知公理"
- 如果项目需要简化纪律，合并"马斯克 5 步法"
- 为了更好的代码质量，合并"Karpathy 原则"

### 方式 3：定制化
文件是模块化的。保留适合你工作流的部分：
- **认知公理**：用于复杂决策和系统设计
- **5 步法**：避免过度工程
- **Karpathy 原则**：代码质量和可维护性
- **数据完整性**：严格准确性要求的项目
- **安全防护**：生产系统

## 与众不同之处

大多数 CLAUDE.md 文件关注"如何编码"。这个关注**"如何思考"** 然后再编码：

1. **认知基础**：基于普世原则（熵、进化、涌现）而非编码惯例
2. **质疑优先文化**：系统性挑战需求（马斯克方法）
3. **外科手术式精准**：只触碰必须改变的（Karpathy 原则）
4. **验证执行**：每一步都有成功标准
5. **透明的不确定性**：从不猜测或美化数据

## 核心概念

### 第一性原理思维
剥离惯例和类比。从基本真理（物理、数学、逻辑）推导解决方案。

### 5 步执行优先级
1. 质疑必要性
2. 删除非必要项
3. 简化剩余部分
4. 加速周期
5. 最后自动化

### 数据完整性
- 从不根据不清晰的图像猜测
- 从不为报告美化数据
- 始终展示计算过程
- 立即承认错误

### 外科手术式修改
- 每行变更都追溯到用户请求
- 完全匹配现有风格
- 不"改进"相邻代码
- 只清理你的修改产生的孤儿代码

## 示例

**之前**（典型 LLM 行为）：
```
用户："给登录表单添加验证"
Claude：[添加验证 + 重构表单组件 + 更新样式 + 添加未使用的错误状态]
```

**之后**（使用这些指令）：
```
用户："给登录表单添加验证"
Claude："我会添加邮箱/密码验证。计划：
1. 添加验证规则 → 用无效输入测试
2. 显示错误消息 → 测试错误显示
3. 无效时阻止提交 → 测试提交拦截

我还应该处理边界情况如空字符串吗，还是只做基本格式验证？"
[只做请求的修改，匹配现有代码风格]
```

## 权衡

这些指南**偏向谨慎而非速度**。它们设计用于：
- 非琐碎功能
- 生产系统
- 需长期维护的代码
- 多人协作项目

对于简单的拼写修复或单行修改，使用你的判断力。

## 相关工作

- **Karpathy 的观察**：[关于 LLM 编码错误的推文](https://x.com/karpathy/status/2015883857489522876)
- **马斯克的工程方法论**：来自 SpaceX/Tesla 制造的第一性原理思维
- **BMAD-METHOD**：完整的 SDLC 工作流（PM → 架构师 → 开发 → QA）
- **claude-code-bmad-foundation**：结合 Karpathy + BMAD 的模板

## 贡献

这是一个活文档。如果你发现改进点：
1. 开 issue 说明你的使用场景
2. 分享什么有效、什么无效
3. 用清晰的推理提出补充

## 快速开始

```bash
# 1. 复制 CLAUDE.md 到你的项目
curl -o CLAUDE.md https://raw.githubusercontent.com/AIPMAndy/andy-claude-directives/main/CLAUDE.md

# 2. 或使用特定模板
curl -o CLAUDE.md https://raw.githubusercontent.com/AIPMAndy/andy-claude-directives/main/TEMPLATES.md
# 然后从文件中选择一个模板

# 3. 为你的项目定制
# 编辑 CLAUDE.md，添加你的技术栈和项目规则
```

## 文档

- 📖 **[模板集合](./TEMPLATES.md)** - 6 个针对不同场景的预配置模板
- 💡 **[使用示例](./EXAMPLES.md)** - 前后对比展示真实行为变化
- 🇨🇳 **[中文文档](./README_CN.md)** - 完整中文文档

## Star 历史

如果这对你有帮助，请考虑给个 star ⭐

[![Star History Chart](https://api.star-history.com/svg?repos=AIPMAndy/andy-claude-directives&type=Date)](https://star-history.com/#AIPMAndy/andy-claude-directives&Date)

## 社区

- **分享成功案例**：[使用此模板](./.github/ISSUE_TEMPLATE/success_story.md)
- **报告问题**：[Bug 报告模板](./.github/ISSUE_TEMPLATE/bug_report.md)
- **建议改进**：[改进建议模板](./.github/ISSUE_TEMPLATE/improvement.md)

## 许可证

MIT - 自由使用、修改，无需署名。

## 致谢

- **Andrej Karpathy**：揭示常见 LLM 编码失败模式
- **Elon Musk**：5 步工程方法论
- **第一性原理思考者**：认知基础

---

**与 Anthropic、OpenAI 或任何 AI 公司无关。**  
只是一个开发者让 Claude Code 更系统可靠的尝试。

## 支持项目

如果你觉得有价值：
- ⭐ 给仓库点星
- 🐦 在 [Twitter/X](https://twitter.com/intent/tweet?text=推荐%20Andy%27s%20Core%20Operating%20Directives%20for%20Claude%20Code%20-%20结合认知公理、马斯克方法论和%20Karpathy%20原则&url=https://github.com/AIPMAndy/andy-claude-directives) 分享
- 💬 在 Issues 分享你的成功案例
- 🤝 通过 PR 贡献改进
