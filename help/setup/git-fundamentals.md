---
title: Git 和 GitHub 文档要点
description: 本文概述了 Git、GitHub 存储库、内容的组织方式以及用于 Adobe 文档的命名约定。
exl-id: 2b2ec764-4201-4bcd-802d-a034d6675793
source-git-commit: 90122796acee9214ba96360eb7b5ff5c321a4bd6
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 100%

---

# Git 和 GitHub 文档要点

## 概述

如果您只需要对文章进行次要的纯文本更改，则无需了解本文的详细信息。本文介绍了进行主要编辑的工作流，例如创建新文章、添加图像或对 Adobe 文档进行持续编辑。

作为 Adobe 文档内容的参与者，您可以与多个工具和流程进行交互。您可以与其他参与者同时处理同一项目，可以是完全相同的内容，甚至可以在同一时间。这一切都可以通过 Git 和 GitHub 软件实现。

Git 是一个允许协作的开源版本控制系统。多个参与者可以处理&#x200B;*存储库*&#x200B;中的文件。

GitHub 是用于 Git 存储库的基于 Web 的托管服务，例如用于存储 [docs.adobe.com](https://docs.adobe.com) 内容的托管服务。对于任何项目，GitHub 都会托管主存储库，参与者可以在其中创建自己的作品副本。

## Git

Git 具有独特的参与工作流和术语，可支持其分布式模型。例如，没有通常与签出/签入操作相关联的文件锁定流程。Git 允会逐字节地比较文件，从而可以在更精细的级别上解决更改。

Git 还使用分层结构来存储和管理项目的内容：

- *存储库*: 英文简称为 *repo*，是存储结构最顶部的单元。存储库包含一个或多个分支。
- *分支*：所有存储库都包含一个默认分支（一般称为“主分支”）和要合并回主分支中的一个或多个分支。主分支作为当前版本和从其发布内容的来源。它是创建存储库中所有其他分支的父级存储库。

参与者可与 Git 交互以更新和处理本地和 GitHub 两个级别的存储库：

- 在本地通过 GitHub Desktop 等工具。
- 通过 [www.github.com](https://www.github.com)，它集成了 Git 以管理流回主存储库中的稿件协调。

## GitHub

所有工作流都在 GitHub 级别开始和结束，GitHub 可存储任何 Adobe 文档项目的主存储库。参与者所创建的供自己使用的副本分布在多台计算机上。系统最终会将这些副本重新调整回项目的主 GitHub 存储库中。

### 目录组织

项目的默认/主分支作为该项目的内容的当前版本。主分支和从其创建的分支中的内容与文章主题的组织一致。子目录用于组织内容和图像资产。

您通常可以在存储库的根下找到主 `help` 目录。文章目录包含一组子目录。子目录中的文章会格式化为使用 *.md* 扩展名的 Markdown 文件。

在此目录的根下，您可以找到与整个服务或产品相关的一般性文章。通常，随后您可以找到与功能/服务或常见方案匹配的其他系列子目录。

### 资产目录

用户指南目录包含用于目录中引用的图像文件的 `/assets` 子目录。

<!--

### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. It also includes SEO optimizations and reporting processes that Adobe uses to evaluate the performance of the content. So the metadata is important!
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of docs.adobe.com extensions**, which you can use for special controls such as buttons and selectors.

-->

## 拉取请求

通过&#x200B;*拉取请求*，参与者可以非常方便地提出一组将应用于默认分支的更改。更改（也称为&#x200B;*提交*）存储在参与者的分支中，因此 GitHub 可以先对将它们&#x200B;*合并*&#x200B;到默认分支中所产生的影响进行建模。拉取请求还可以作为一种机制，通过构建/验证过程（即拉取请求审核人员）为参与者提供反馈，以便在将更改合并到默认分支之前解决潜在的问题。

根据您提议的更改的规模，可以通过拉取请求进行两种方式的参与。我们稍后将在本指南的 [GitHub 工作流](local-repo.md)部分详细介绍此内容。
