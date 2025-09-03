# 🏠 Smiddy's Corner - How-To Repository

<div align="center">

[![Azure DevOps Board](https://img.shields.io/badge/Azure%20DevOps-Boards-0078d4?style=for-the-badge&logo=azure-devops)](https://dev.azure.com/MngEnvMCAP731175/201e473b-14a4-492c-8d66-26b9d951bf22/_boards/board/t/23ada9f4-f8d9-4280-92d3-0176bbd6b1f9/Issues/)
[![PowerPlatform](https://img.shields.io/badge/Power%20Platform-CLI-742774?style=for-the-badge&logo=microsoft)](./PowerPlatform/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

**🎯 A comprehensive collection of tips, tricks, and how-to guides for developers and IT professionals**

</div>

---

## 📋 Table of Contents

- [🎯 About](#-about)
- [🔧 Azure DevOps Integration](#-azure-devops-integration)
- [⚡ Power Platform Resources](#-power-platform-resources)
- [🚀 Getting Started](#-getting-started)
- [📖 Documentation](#-documentation)
- [⚠️ Important Notice](#️-important-notice)

---

## 🎯 About

Welcome to **Smiddy's Corner**! This repository serves as a centralized hub for practical how-to guides, code samples, and best practices across various Microsoft technologies and development workflows.

### 🌟 What You'll Find Here:

- 📊 **Azure DevOps** integration examples and workflows
- ⚡ **Power Platform** CLI automation scripts
- 🔄 **CI/CD Pipeline** templates and configurations  
- 💡 **Tips & Tricks** from real-world implementations
- 📚 **Step-by-step guides** for common development scenarios

---

## 🔧 Azure DevOps Integration

This repository demonstrates comprehensive **Azure DevOps Boards** integration, showcasing modern project management and development workflow practices.

### 📊 Live Board Status

[![Board Status](https://dev.azure.com/MngEnvMCAP731175/201e473b-14a4-492c-8d66-26b9d951bf22/23ada9f4-f8d9-4280-92d3-0176bbd6b1f9/_apis/work/boardbadge/118ab748-63a3-49ab-b686-ab4b5911d166)](https://dev.azure.com/MngEnvMCAP731175/201e473b-14a4-492c-8d66-26b9d951bf22/_boards/board/t/23ada9f4-f8d9-4280-92d3-0176bbd6b1f9/Issues/)

*Click the badge above to view the live Azure DevOps board*

### 🔗 Key Integration Features:

| Feature | Description | Benefit |
|---------|-------------|---------|
| 🎯 **Work Item Tracking** | Automatic linking between commits and work items using `AB#` syntax | Seamless traceability from code to requirements |
| 📈 **Board Badges** | Real-time status indicators embedded in README | Instant visibility of project health |
| 🔄 **Automated Workflows** | CI/CD pipelines triggered by board state changes | Streamlined development lifecycle |
| 📝 **Commit Linking** | Direct references like `[AB#175]` in commit messages | Enhanced project transparency |

### 💡 How to Implement Azure DevOps Boards Integration:

1. **Enable Board Badges:**
   ```markdown
   [![Board Status](YOUR_BOARD_BADGE_URL)](YOUR_BOARD_URL)
   ```

2. **Link Work Items in Commits:**
   ```bash
   git commit -m "Fix authentication issue AB#175"
   ```

3. **Reference Work Items in Pull Requests:**
   - Use `Fixes AB#175` to automatically close work items
   - Use `Related to AB#175` for general references

---

## ⚡ Power Platform Resources

Explore our comprehensive **Power Platform CLI** automation examples and pipeline configurations.

### 📁 Available Resources:

- 🔧 [**PowerPlatform CLI Setup**](./PowerPlatform/PowerPlatform.md) - Complete pipeline configuration
- 🚀 **Automated Deployment** scripts for Power Platform solutions
- 📋 **YAML Pipeline** templates for Azure DevOps
- 🔐 **Security Best Practices** for authentication and secrets management

### 🎯 Quick Start:

```bash
# Navigate to Power Platform examples
cd PowerPlatform/

# Review the automation guide
cat PowerPlatform.md
```

---

## 🚀 Getting Started

### 📋 Prerequisites:

- 🔹 Azure DevOps account with board access
- 🔹 Power Platform environment (for Power Platform examples)
- 🔹 Git knowledge for version control
- 🔹 Basic PowerShell/CLI experience

### 🎯 Quick Setup:

1. **Clone this repository:**
   ```bash
   git clone https://github.com/Smiddy4000/HowTo.git
   cd HowTo
   ```

2. **Explore the content:**
   ```bash
   # View Power Platform automation
   ls PowerPlatform/
   
   # Check current board status
   # Visit the board badge link above
   ```

3. **Start implementing:**
   - Follow the guides in each directory
   - Adapt examples to your environment
   - Contribute improvements back to the community

---

## 📖 Documentation

### 🗂️ Repository Structure:

```
HowTo/
├── 📄 README.md              # This comprehensive guide
├── 📁 PowerPlatform/         # Power Platform CLI examples
│   └── 📄 PowerPlatform.md   # Detailed automation guide
└── 🔧 .git/                 # Git configuration
```

### 🔗 External Resources:

- 📊 [Azure DevOps Boards Documentation](https://docs.microsoft.com/en-us/azure/devops/boards/)
- ⚡ [Power Platform CLI Reference](https://docs.microsoft.com/en-us/power-platform/developer/cli/reference/overview)
- 🔄 [Azure DevOps YAML Pipeline Schema](https://docs.microsoft.com/en-us/azure/devops/pipelines/yaml-schema/)

---

## ⚠️ Important Notice

> [!IMPORTANT]
> **All code and examples in this repository are provided for educational and illustration purposes only.**

> [!WARNING]  
> **These examples are NOT intended for production use without proper review, testing, and adaptation to your specific environment.**

### 📋 Disclaimer:

```
THIS CODE AND ANY RELATED INFORMATION ARE PROVIDED "AS IS" WITHOUT WARRANTY 
OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE 
IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.
```

---

<div align="center">

### 🤝 Contributing

Found an issue? Have a suggestion? Feel free to:

[![Open Issue](https://img.shields.io/badge/Open-Issue-red?style=for-the-badge&logo=github)](https://github.com/Smiddy4000/HowTo/issues)
[![Submit PR](https://img.shields.io/badge/Submit-Pull%20Request-green?style=for-the-badge&logo=github)](https://github.com/Smiddy4000/HowTo/pulls)

---

**Made with ❤️ by Smiddy | Follow the Azure DevOps board for latest updates**

</div>