---
title: Adobe 文档参与者指南
seo-title: Adobe Experience Cloud 技术文档的参与者指南概览
description: 该指南介绍了如何向 Adobe 文档站点提供建议和添加内容。
seo-description: 该指南介绍了如何向 [!UICONTROL Adobe Experience Cloud] 技术文档投稿。
translation-type: ht
source-git-commit: 8943af2fdf406b2e33db037bb60dfea97df2959a
workflow-type: ht
source-wordcount: '837'
ht-degree: 100%

---


# Adobe 文档的参与者指南概览

## 什么是协作文档

2019 年，根据开源原则并利用 Github、Markdown 和 Adobe Experience Cloud 解决方案（其中包括 Adobe Experience Manager、Analytics、Launch 和 Target），Adobe Experience Cloud 的所有技术文档和支持内容正在过渡到一个崭新的平台。

这种开源模型提升了内容质量，并且加强了客户、文档团队和产品团队之间的沟通。如今，您在每个页面上都可以评价内容实用性、记录问题，甚至可以将有关的内容建议作为 Git 拉取请求 (PR) 进行投稿。Adobe 文档团队每天都在检查投送的稿件和有关问题，并且会根据需要进行更新和调整。

## 与“协作文档”团队合作

作为本材料的用户 - 无论您是员工、合作伙伴、客户还是潜在客户 - 您都可以选择采取以下几种简便的方式，为这类文档投稿：

* 评价页面的实用性
* 针对特定页面，记录相关问题
* 您甚至还可以这样 - 提交一些快速编辑的内容，进而可以创作整篇文章，并利用一些资产和代码示例来完成相应的稿件

关于如何与这类文档材料小组进行互动以及如何投稿，本指南概述了您需要了解的所有相关内容。

<!--
>[!IMPORTANT]
>All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
-->

## 对现有文档进行快速编辑

快速编辑非常适合修复文档中的小错误和遗漏。如果文章显示如下所示的编辑按钮，您可以自己进行快速修复。编辑文档时，您可以提交拉取请求 (PR) 以向我们提交修复/建议，之后，我们可以检查、批准和发布建议。

1. 签署[参与者许可协议 (CLA)](http://opensource.adobe.com/cla.html)（如果接受）。

   您只需提交一次 Adobe CLA 即可。
1. 单击右列的 **`Edit this page`** 图标以转到 GitHub 上的 Markdown 源文件。

   ![编辑此页面图标](/help/assets/git_edit.png)

1. 单击铅笔图标可编辑相关文章。

   >[!NOTE]
   >
   >如果铅笔图标呈灰显状态，则表明您需要登录您的 GitHub 帐户，或创建一个新帐户。

   ![铅笔图标的位置](assets/edit-icon.png)

1. 在 Web 编辑器中进行更改。您可以单击 **Preview changes**（预览更改）选项卡以检查所做更改的格式。
1. 完成更改后，滚动到页面底部。输入 PR 的标题和描述，然后单击 **Propose file change**（建议文件更改），如下图所示：

   ![提出更改建议](assets/submit-pull-request.png)

   >[!NOTE]
   >
   >如果您收到有关签署“参与者许可协议”(CLA) 的验证错误消息，请单击 **Details**（详细信息），以打开相关的许可协议。签署协议（如果接受）。接下来，关闭并打开拉取请求，然后继续操作。

以上就是所有步骤。谢谢！文档团队成员将审核并合并您的拉取请求。

## 记录问题

让我们了解某段内容中问题的另一种简单方法是“记录问题”。

1. 如果您看到某段内容有问题，请单击右列的 **`Log an Issue`** 图标。

   ![](assets/git_log_issue.png)

   >[!NOTE]
   >
   >您需要登录 GitHub 帐户或创建一个新帐户来记录问题。

   通过单击此链接，您可以使用“Github 问题”界面与我们一起快速记录问题。

1. 描述字段中将自动填充存在问题的页面的 URL。填写标题，简要描述问题，然后单击 *Submit new issue*（提交新问题）。

   ![](assets/git_issue_example.png)

提交问题后，系统将会直接通知负责该页面的内容团队，以便他们能够采取相应措施。更新内容后，我们会通过“Github 问题”界面通知您，并且会在内容更新或关闭时通过电子邮件通知您。

## 了解 GitHub 权限

GitHub 编辑 UI 会根据您的存储库权限自行调整。对于不具有目标存储库写入权限的参与者，前面的图像是准确的。GitHub 会自动在您的帐户中创建目标存储库分支。如果您具有目标存储库的写入权限，GitHub 会在目标存储库中创建一个新分支。

Adobe 会对所有更改使用拉取请求，甚至对于具有写入权限的参与者也是如此。大多数存储库都会保护 `master` 分支，因此必须作为拉取请求来提交更新。

浏览器内编辑体验最适用于次要或不常见的更改。如果您要进行大量更改或使用高级 Git 功能，我们建议您[创建分支存储库并在本地使用](setup/full-workflow.md)。

## 提供反馈

要设置与 Adobe 一样大型的解决方案，文档工作始终任重而道远。如果发现错误，请将问题记录下来；如果想提供有关材料的建议，请告知我们。告诉我们您需要的信息。如果您无法找到所需内容，请告知我们；或者如果您在完成任务时遇到困难，请告诉我们可以如何帮助您了解我们的解决方案。

在此，请接受“协作文档”团队和 [!UICONTROL Adobe Experience Cloud] 全体作者及内容制作人员的真诚谢意。
