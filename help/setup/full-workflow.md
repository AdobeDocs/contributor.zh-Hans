---
lastModified: 2018-06-28T00:00:00Z
title: 针对主要更改的 GitHub 参与工作流
seo-title: 针对 Adobe 文档的主要更改的 GitHub 参与工作流
description: 本文会向您介绍如何使用“主要”参与者工作流参与 adobe 文档的编写。
seo-description: 本文会向您介绍如何使用“主要”参与者工作流参与 adobe 文档的编写。
translation-type: ht
source-git-commit: 6ec1d13f80698cb5963c07656ef8183db735ff75
workflow-type: ht
source-wordcount: '976'
ht-degree: 100%

---


# 针对主要更改的 GitHub 参与工作流

<!--
>[!IMPORTANT]
>All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
--->

## 概述

此工作流适合需要做出主要更改或将经常向存储库投稿的参与者。经常投稿的参与者通常会不断（持续时间长）做出更改，这些更改将经历多个周期（构建/验证/分段）或在签发和合并拉取请求之前跨越多日。

### 术语

在开始之前，我们先看看此工作流中所使用的 Git/GitHub 术语。

| 名称 | 描述 |
|-----------|-------------|
| 分支存储库 | 在指主 GitHub 存储库的副本时，通常用作名词。实际上，分支存储库只是另一个存储库。但从 GitHub 维护主/父存储库的双向连接的意义上来讲，这个词具有特殊意义。有时它也用作动词，例如“必须先创建分支存储库”。 |
| 远程存储库 | 用于远程存储库的命名连接，例如“原始”或“上游”远程存储库。Git 将它们称为远程存储库，因为它们用于引用其他计算机上托管的存储库。在此工作流中，远程存储库始终表示 GitHub 存储库。 |
| 原始存储库 | 分配给本地存储库与其克隆存储库之间关系的名称。在此工作流中，原始存储库表示与您的分支存储库的关系。它有时被用作原始存储库本身的名字对象，如“记住将更改推送到原始存储库”。 |
| 上游存储库 | 与原始远程一样，上游存储库是与另一个存储库的命名关系。在此工作流中，上游存储库代表本地存储库与从中创建分支存储库的主存储库之间的关系。有时，它被用作上游存储库本身的名字对象，例如“记住从上游存储库中提取更改”。 |

如果您不熟悉 Git 和 GitHub 概念（如存储库或分支），请先查看 [Git 和 GitHub 基础知识](git-fundamentals.md)。

## 工作流

>[!IMPORTANT]
> 如果还没有工作流，则必须完成[设置](github-signup.md)部分中的步骤。

在此工作流中，更改重复循环流入。从您设备的本地存储库开始，它们将流回您的 GitHub 分支存储库，进入主 GitHub 存储库，并在您合并其他参与者所做的更改时再次从本地返回。

### 使用 GitHub 流

回顾 [Git 和 GitHub 基础知识](git-fundamentals.md)，Git 存储库包含一个主分支，以及尚未集成到主存储库中的任何其他进程中的分支。每当您想引入一组逻辑上相关的更改时，最佳做法是创建&#x200B;*工作分支*&#x200B;以通过工作流管理您所做的更改。我们此时将它称为工作分支，这是因为在将它们可以集成到主分支中之前，它是一个用于迭代/优化更改的工作区。

通过隔离特定分支的相关更改，您可以单独控制和引入这些更改，将这些更改定位到发布周期中的特定发布时间。实际上，根据您所从事的工作类型，您可以轻松地在存储库中使用多个工作分支。在同一时间使用多个分支并不罕见，各个分支代表各个不同的项目。

>[!NOTE]
>
>在主分支中进行更改&#x200B;*不是最佳做法*。假设您使用主分支为定时功能发布引入一组更改。您已完成更改并正等待发布它们。在此期间，您收到一个紧急请求，需要修复某些内容，因此您先更改了主分支中的文件，然后再发布更改。在此示例中，您既无意中发布了修复&#x200B;*，又发布了*&#x200B;您原本计划在特定日期发布的更改。

接下来，在本地存储库中创建一个新的工作分支，以获取您提议的更改。每个 git 客户端各不相同，因此请咨询首选客户端的帮助。您可以在 [GitHub 流](https://guides.github.com/introduction/flow/)的 GitHub 指南中查看该过程的概述。

## 拉取请求处理

您可以提交建议的更改，方法是通过将它们捆绑在添加到目标存储库的 PR 队列的新拉取请求 (PR) 中。拉取请求会启用 GitHub 的协作模型，方法是请求将工作分支的更改拉入并合并到另一个分支。在大多数情况下，另一个分支是主存储库中的默认/主分支。

### 验证

在将拉取请求合并到目标分支之前，可能需要通过一个或多个 PR 验证过程。验证过程可能会有所不同，具体取决于建议的更改范围和目标存储库的规则。提交拉取请求后，您可以审核内容，并在适当时将其合并到主存储库中。

### 审核和注销

完成所有 PR 处理后，您应审核结果（PR 注释、预览 URL 等）以确定是否需要先对其文件进行其他更改，然后再签发以进行合并。在 PR 审核人员审核了您的拉取请求后，如果在合并之前具有待解决的问题，他们也可以通过添加注释的方式提供反馈。

当拉取请求没有问题并签发后，系统会将您的更改合并回父分支，并且关闭拉取请求。

### 发布

请记住，您的拉取请求必须先由 PR 审核人员合并，然后才能将更改包含在下一个预定发布运行中。通常，审核人员会按提交顺序审核/合并拉取请求。如果需要先合并您的拉取请求才能将其包含在特定的发布运行中，您需要提前与 PR 审核人员展开合作，以确保在发布之前进行合并。
