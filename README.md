<div align="center">

# .gitignore 模板合集 中文翻译版

**[中文版] .gitignore 模板合集 — GitHub 官方 .gitignore 模板库的中文版**

[![原项目](https://img.shields.io/badge/原项目-github--gitignore-blue?style=flat-square&logo=github)](https://github.com/github/gitignore)
[![中文文档](https://img.shields.io/badge/中文文档-README.zh--CN.md-orange?style=flat-square)](README.zh-CN.md)
[![GitHub Stars](https://img.shields.io/github/stars/github/gitignore?style=flat-square&label=原项目Stars)](https://github.com/github/gitignore/stargazers)
[![微信联系](https://img.shields.io/badge/微信-uaycar-brightgreen?style=flat-square&logo=wechat)](#)

</div>

---

> 这是 [github/gitignore](https://github.com/github/gitignore) 的中文翻译版本。
> 完整源代码请访问原项目:https://github.com/github/gitignore

**代部署 / 定制服务 / 技术咨询 请添加微信:uaycar**

---

## 📖 项目简介

这是 GitHub 官方维护的 `.gitignore` 文件模板合集。当你在 GitHub 网页上新建仓库或新建文件时,界面上那个 .gitignore 模板选择器,内容正是由这个仓库填充的。它覆盖主流编程语言、框架、编辑器与操作系统,帮你避免把编译产物、依赖目录、本地配置等不该提交的文件推进仓库。

## ✨ 主要特性

- 🏛️ **GitHub 官方维护**,直接服务于 GitHub 网页端的模板选择器,权威且持续更新
- 📚 **根目录主流模板**:Node、Python、Java、Go、Rust、C++、CMake、Swift 等常用技术栈开箱即用
- 🖥️ **Global 目录**:Windows、macOS、Linux 操作系统模板,以及 JetBrains、VSCode、Sublime Text、Vim、Emacs 等编辑器模板
- 🧩 **community 目录**:收录大量小众语言、框架与工具的专项模板,按目录分类
- 🔍 **精选而非大而全**:每个模板都是一套小而实用的规则,避免无意义的巨型清单
- 🧬 **版本化模板策略**:根目录永远是当前支持版,旧版本放进 community 并带版本号命名
- 📄 **CC0-1.0 许可**:可自由复制、修改、商用,无任何附加条件

## 📁 文件说明

| 文件 | 说明 |
|:-----|:-----|
| README.md | 本文件(中文简介) |
| README.zh-CN.md | 详细中文文档(完整汉化) |

## 🚀 快速开始

1. 打开原项目仓库,按语言/工具找到对应模板(如根目录的 `Node.gitignore`)
2. 把模板内容复制到你项目的根目录下,重命名为 `.gitignore`
3. 需要时把多个模板合并(语言模板 + 编辑器模板 + 操作系统模板)
4. 想对本机所有仓库生效,可配置全局忽略文件:

```bash
git config --global core.excludesfile ~/.gitignore_global
```

5. 也可以通过 GitHub API 直接拉取模板内容:

```bash
curl https://api.github.com/repos/github/gitignore/contents/Node.gitignore
```

6. 提交前用 `git status` 或 `git check-ignore -v <文件>` 验证忽略规则是否生效

完整源代码与最新版本请访问原项目:https://github.com/github/gitignore

## 📞 联系方式

**代部署 / 定制服务 / 技术咨询 请添加微信:uaycar**

---

本项目为 [github/gitignore](https://github.com/github/gitignore) 的中文翻译版本,所有模板与内容版权归原项目作者所有,遵循其原始许可证(CC0-1.0)。

**如果觉得有用,请给原项目点个 Star!** ⭐
