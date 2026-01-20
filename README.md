# rpp-multi
# RPP MULTI Language Support

Compiled at: 2026-01-20 12:37:33

[English](#english) | [中文](#中文)

Contributors: Fuyuan Wu(fuyuan.wu@sjtu.edu.cn),Rafael Ramis(rafael.ramis@upm.es)

## 中文

完整的RPP/MULTI语言支持扩展，提供语法高亮、实时诊断和错误检查功能。

### 功能特性

- ✨ **语法高亮** - 支持RPP/MULTI语言的语法着色
- 📋 **实时诊断** - 编辑时立即检测常见错误
- 🔍 **缺少分号检查** - 自动检测语句缺少分号
- 💡 **快速修复** - 提供一键修复建议
- 🎯 **智能识别** - 识别`.r`和`.rpp`文件
- ⚙️ **语言配置** - 括号匹配、自动缩进、注释符号

### 安装

1. VS Code扩展市场搜索 `rpp.multi`
2. 或在工作目录运行：`npm install` 后按 `F5` 调试运行

### 快速开始

打开任何 `.r` 或 `.rpp` 文件，扩展自动激活并提供实时诊断。

### 开发环境设置

```bash
cd rpp.multi-20260120-1.0.2
npm install
npm run compile
npm run watch  # 监视模式
```

### 打包和发布

```bash
npm run package  # 生成VSIX包
vsce publish     # 发布到VS Code Marketplace
```

### 诊断规则

检查以下条件的语句是否缺少分号：
- 不以 `;` 结尾
- 不以 `{` 结尾（代码块开始）
- 不以 `,` 结尾（参数列表）
- 非注释行（以`$`开头）
- 非空行
- 非语句延续行

### 许可证

MIT License

---

## English

Complete RPP/MULTI language support extension with syntax highlighting, real-time diagnostics, and error checking.

### Features

- ✨ **Syntax Highlighting** - RPP/MULTI language syntax coloring
- 📋 **Real-time Diagnostics** - Instant error detection while editing
- 🔍 **Missing Semicolon Check** - Automatic detection
- 💡 **Quick Fix** - One-click suggestions
- 🎯 **Smart Recognition** - Support for `.r` and `.rpp` files
- ⚙️ **Language Configuration** - Bracket matching, auto-indent

### Installation

1. Search for `rpp.multi` in VS Code Extensions marketplace
2. Or run `npm install` then press `F5` to debug

### Quick Start

Open any `.r` or `.rpp` file. The extension activates automatically with real-time diagnostics.

### Development Setup

```bash
cd rpp.multi-20260120-1.0.2
npm install
npm run compile
npm run watch  # Watch mode
```

### Packaging and Publishing

```bash
npm run package  # Generate VSIX package
vsce publish     # Publish to VS Code Marketplace
```

### Diagnostic Rules

Statements are checked for missing semicolons if they:
- Don't end with `;`
- Don't end with `{` (code block start)
- Don't end with `,` (parameter list)
- Are not comment lines (starting with `$`)
- Are not empty lines
- Are not statement continuation lines

### License

MIT License
