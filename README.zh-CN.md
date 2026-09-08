<div align="center">

# .gitignore 模板合集 中文文档

**[中文版] .gitignore 模板合集 — GitHub 官方 .gitignore 模板库的中文版**

[![原项目](https://img.shields.io/badge/原项目-github--gitignore-blue?style=flat-square&logo=github)](https://github.com/github/gitignore)
[![中文简介](https://img.shields.io/badge/中文简介-README.md-orange?style=flat-square)](README.md)
[![微信联系](https://img.shields.io/badge/微信-uaycar-brightgreen?style=flat-square&logo=wechat)](#)

</div>

> 本文档是 [github/gitignore](https://github.com/github/gitignore) 官方 README 的中文翻译版本,并附常用模板一览。**代部署 / 定制服务 / 技术咨询 请添加微信:uaycar**

---

## 一份 `.gitignore` 模板合集

这是 GitHub 官方收集的 [`.gitignore`](https://git-scm.com/docs/gitignore) 文件模板库。GitHub 用这份清单来填充 GitHub.com 界面中"创建新仓库 / 新建文件"时的 `.gitignore` 模板选择器。

想深入了解 `.gitignore` 文件的工作原理和用法,下面这些资源是很好的起点:

- 《[Pro Git](https://git-scm.com/book)》一书中"忽略文件"章节
- GitHub 帮助站点上的"忽略文件"文章
- `gitignore(5)` 手册页:https://git-scm.com/docs/gitignore

## 目录结构

官方支持的模板按如下方式组织:

- **根目录**:收录通用模板,帮助用户快速上手主流编程语言和技术。这些模板定义了一套有实际意义的规则,既能帮你快速起步,也能确保你不会把无关紧要的文件提交进仓库。
- **[`Global`](https://github.com/github/gitignore/tree/main/Global)**:收录各类编辑器、工具和操作系统的模板,适用于不同场景。建议把它们加入你的全局模板,或在你确定要长期使用时,把这些规则合并进项目专属模板。
- **[`community`](https://github.com/github/gitignore/tree/main/community)**:收录其他流行语言、工具和项目的专项模板——它们目前还不适合进入主流模板。当你决定采用某个框架或工具时,再把它们加进自己的项目模板。

## 什么样的模板才算好模板?

首先,模板贡献必须遵守官方的[贡献指南](https://github.com/github/gitignore/blob/main/CONTRIBUTING.md)。

一个模板应当包含一组规则,帮助 Git 仓库与某种特定的编程语言、框架、工具或环境配合工作。如果针对某种情况无法精选出一小组有用的规则,那它就不适合收进这个合集。

如果模板的大部分内容只是某个软件特定版本所安装文件的列表(例如某个 PHP 框架),它可以放在 `community` 目录下,详见下文"版本化模板"。

如果你只有一小组规则,或想支持一项使用还不广泛的技术,但仍然相信它对他人有帮助,请阅读"专项模板"一节。

在提交 PR 时,如果模板比较重要且可见,请附上详细说明。官方不一定立即接受,但日后可以根据关注度把它提升到根目录。

另外请理解:官方不可能收录曾经存在过的每一个工具。它的目标是精选**最常见、最有帮助**的模板,而不是覆盖所有项目。如果官方没有收录你的语言、工具或项目,不代表它不优秀。

## 版本化模板

有些模板在不同版本之间差异很大。想给本仓库做贡献的话,需要遵循这样的流程:

- 根目录的模板应当是当前受支持的版本
- 根目录模板的文件名不应带版本号(即"常青"命名)
- 模板的旧版本应放在 `community/` 下
- 旧版本的文件名中应嵌入版本号,便于辨认

这样既保证用户拿到的是最新版本(他们会直接用根目录那份),也让维护者能继续支持仍在使用旧版本的用户。

## 专项模板

如果你有一个想贡献、但还不够主流的模板,请把它放进 `community` 目录下最合适的子目录。

专项模板中的规则应只针对该框架或工具本身,如有需要搭配的其他模板,应在模板开头的注释中注明。例如一个模板可能位于 `community/DotNet/InforCRM.gitignore`:

```gitignore
# gitignore template for InforCRM (formerly SalesLogix)
# website: https://www.infor.com/product-summary/cx/infor-crm/
#
# Recommended: VisualStudio.gitignore

# Ignore model files that are auto-generated
ModelIndex.xml
ExportedFiles.xml

# Ignore deployment files
[Mm]odel/[Dd]eployment

# Force include portal SupportFiles
!Model/Portal/*/SupportFiles/[Bb]in/
!Model/Portal/PortalTemplates/*/SupportFiles/[Bb]in
```

## 常用模板一览(代表性条目)

| 类别 | 代表模板 | 典型忽略内容 |
|:-----|:---------|:-------------|
| 语言/运行时 | `Node.gitignore`、`Python.gitignore`、`Java.gitignore`、`Go.gitignore`、`Rust.gitignore` | `node_modules/`、`__pycache__/`、`*.class`、`target/` 等 |
| C/C++ | `C++.gitignore`、`CMake.gitignore` | `build/`、`*.o`、`CMakeFiles/` 等 |
| 前端 | `Vue.gitignore`、`Node.gitignore` | `dist/`、`.npm`、`node_modules/` 等 |
| 移动端 | `Android.gitignore`、`Swift.gitignore`、`Flutter.gitignore` | `build/`、`*.apk`、`Pods/` 等 |
| 游戏引擎 | `Unity.gitignore`、`UnrealEngine.gitignore`、`Godot.gitignore` | `Library/`、`Saved/`、`.godot/` 等 |
| IDE | `Global/JetBrains.gitignore`、`Global/VisualStudioCode.gitignore`、`Global/SublimeText.gitignore` | `.idea/`、`.vscode/` 等工作区文件 |
| 操作系统 | `Global/macOS.gitignore`、`Global/Windows.gitignore`、`Global/Linux.gitignore` | `.DS_Store`、`Thumbs.db` 等 |
| 数据科学 | `JupyterNotebooks.gitignore`、`R.gitignore` | `.ipynb_checkpoints/` 等 |

## 贡献流程

官方建议按以下步骤向本项目提交修改:

1. 把项目 [Fork](https://help.github.com/articles/fork-a-repo/) 到你的账号下
2. 为要做的修改[创建分支](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository)
3. 在你的 Fork 里完成修改
4. 从你的分支向官方 `main` 分支[发起 Pull Request](https://help.github.com/articles/using-pull-requests/)

使用 GitHub 网页界面修改也可以,网页会自动帮你 Fork 并引导你发起 PR。

贡献规范详见官方 [Contributing Guidelines](https://github.com/github/gitignore/blob/main/CONTRIBUTING.md)。

## 许可证

原项目采用 [CC0-1.0](https://github.com/github/gitignore/blob/main/LICENSE) 许可证发布,所有模板可自由使用。

## 使用建议

1. **按需组合**:语言模板 + IDE 模板 + 操作系统模板三者合并,是目前最常见的做法
2. **保持精简**:从对应模板起步,再按项目实际情况追加项目特有规则,避免复制网上来历不明的大段清单
3. **提交前验证**:用 `git check-ignore -v <路径>` 确认规则命中情况,用 `git rm --cached <文件>` 移除已被跟踪的文件
4. **全局配置**:编辑器与操作系统类规则更适合放进全局忽略文件,一次配置、全机生效:

```bash
git config --global core.excludesfile ~/.gitignore_global
```

---

## 版权与致谢

本项目为 [github/gitignore](https://github.com/github/gitignore) 的中文翻译版本,所有模板与内容版权归 GitHub 及各模板贡献者所有,遵循其原始许可证(CC0-1.0)。

**如果觉得有用,请给原项目点个 Star!** ⭐

**代部署 / 定制服务 / 技术咨询 请添加微信:uaycar**
