# MCP Test 1020 - Cherry Studio + GitHub MCP Server 演示

## 📋 项目简介

本仓库用于向**米连集团**的同事演示如何使用 **Cherry Studio** 结合 **GitHub MCP Server** 进行智能化的 GitHub 操作。

通过这个示例，您将学习如何利用 AI 助手自动化完成 GitHub 的各种操作，提升开发效率。

---

## 🎯 演示目标

本演示将展示如何通过 Cherry Studio 的 AI 能力，结合 GitHub MCP (Model Context Protocol) Server，实现以下功能：

- ✅ **仓库管理**：创建、查询、管理 GitHub 仓库
- ✅ **Issue 管理**：创建、查询、更新 Issues
- ✅ **Pull Request 操作**：查看、评审、合并 PR
- ✅ **代码搜索**：跨仓库搜索代码片段
- ✅ **文件操作**：读取、创建、更新文件内容
- ✅ **自动化工作流**：通过自然语言完成复杂的 GitHub 操作

---

## 🚀 快速开始

### 前置要求

1. **Cherry Studio** - AI 驱动的开发工具
2. **GitHub MCP Server** - GitHub 操作的 MCP 协议实现
3. **GitHub Token** - 用于 API 认证

### 安装步骤

#### 1. 安装 Cherry Studio

访问 Cherry Studio 官网下载对应操作系统的版本（支持 macOS / Windows / Linux）

#### 2. 配置 GitHub MCP Server

在 Cherry Studio 的设置中添加 MCP Server 配置：

```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "your_github_token_here"
      }
    }
  }
}
```

#### 3. 获取 GitHub Personal Access Token

1. 访问 GitHub Settings → Developer settings → Personal access tokens
2. 点击 "Generate new token (classic)"
3. 选择所需权限：`repo`、`read:org`、`user`
4. 生成并保存 Token

---

## 💡 使用示例

### 示例 1：查询仓库信息

```
用户：帮我查看 xiadingZ/mcp-test-1020 仓库的详细信息
AI：正在查询仓库信息...
```

### 示例 2：创建 Issue

```
用户：在 mcp-test-1020 仓库创建一个 Issue，标题是"添加使用文档"
AI：已为您创建 Issue #1
```

### 示例 3：搜索代码

```
用户：在我的所有仓库中搜索包含 "pytorch" 的 Python 代码
AI：找到以下相关代码...
```

### 示例 4：创建文件

```
用户：创建一个 example.py 文件，内容是 Hello World 程序
AI：已创建文件并提交...
```

### 示例 5：Pull Request 评审

```
用户：帮我审查 PR #5
AI：正在分析代码质量和测试覆盖...
```

---

## 🎨 核心功能

### 1. 智能仓库管理
- 通过自然语言创建仓库
- 批量查询仓库状态
- 自动生成仓库文档

### 2. Issue 工作流自动化
- 智能创建并关联标签
- 批量更新状态
- 自动分配责任人

### 3. 代码审查助手
- AI 辅助 Code Review
- 自动发现潜在问题
- 生成改进建议

### 4. 文档生成
- 自动生成 README
- 创建 API 文档
- 更新项目文档

---

## 📚 进阶用法 - 完整工作流

**场景**：从需求到发布的完整流程

1. **创建 Feature Issue**："创建用户登录功能的需求 Issue"
2. **创建开发分支**："基于 main 创建 feature/user-login 分支"
3. **实现代码**："创建 user_login.py 实现用户认证"
4. **创建 Pull Request**："创建 PR 合并到 main"
5. **代码审查**："审查 PR 的代码质量"
6. **合并代码**："审查通过后合并 PR"

---

## 🔧 最佳实践

### 安全性
- ⚠️ 不要将 Token 提交到代码仓库
- ✅ 使用环境变量存储敏感信息
- ✅ 定期轮换 Access Token
- ✅ 仅授予必要权限

### 效率提升
- 使用自然语言描述复杂操作
- 批量处理相似任务
- 建立常用操作模板

### 团队协作
- 统一 MCP Server 配置
- 分享最佳实践
- 建立团队操作规范

---

## 🤝 适用场景

### 开发团队
- 代码审查：快速审查 PR
- Issue 管理：自动化分类和分配
- 文档维护：保持文档同步

### 项目管理
- 进度追踪：查询项目状态
- 报告生成：自动生成开发报告
- 资源分配：优化工作分配

### DevOps
- 部署管理：查看发布历史
- 分支管理：维护分支策略
- 自动化流程：集成 CI/CD

---

## 📞 支持与反馈

欢迎通过以下方式联系：
- 创建 Issue
- 提交 Pull Request
- 联系项目维护者

---

## 🌟 致谢

- [Cherry Studio](https://github.com/kangfenmao/cherry-studio) - AI 驱动的开发工具
- [Model Context Protocol](https://modelcontextprotocol.io/) - MCP 协议标准
- [GitHub MCP Server](https://github.com/modelcontextprotocol/servers) - GitHub MCP 实现

---

**演示创建时间**：2024-10-20  
**演示对象**：米连集团技术团队  
**演示目标**：展示 AI 辅助开发工具的强大能力 🚀