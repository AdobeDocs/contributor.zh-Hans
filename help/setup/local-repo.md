---
title: 在本地设置 Git 存储库
description: 本文提供了有关如何创建本地 Git 存储库以及如何对 Adobe 文档做出贡献（包括创建分支存储库和克隆存储库的过程）的指导。
exl-id: 679c07a2-030b-4a30-ba14-7780f88dae11
source-git-commit: a3c283c5c0d181beacc566262743528d5ff9f7d2
workflow-type: ht
source-wordcount: '656'
ht-degree: 100%

---

# 在本地设置适用于文档的 Git 存储库

本文介绍了在本地计算机上设置 git 存储库的步骤，旨在对 Adobe 文档做出贡献。参与者可以使用本地克隆的存储库来添加新文章、对现有文章进行主要编辑或更改作品。

>[!IMPORTANT]
>如果您只对文章进行次要更改，则&#x200B;*不需要*&#x200B;完成本文中的步骤。只需单击“编辑”图标并在浏览器中进行文本编辑即可。

## 概述

要对 Adobe 文档做出贡献，您可以在您自己的 GitHub 帐户中创建相应的分支存储库，以便您具有读/写权限。然后，您可以通过克隆相应的文档存储库在本地创建和编辑 Markdown 文件。然后使用拉取请求将更改合并（提交）到只读中央共享存储库中。

* 确定相应的存储库
* 在您的 GitHub 帐户中创建分支存储库
* 为克隆的文件选择本地文件夹
* 将存储库克隆到您的本地计算机
* 配置上游远程值

## 确定存储库

在您自己的 GitHub 帐户中创建相应的分支存储库，以便您具有在其中存储建议更改的读/写权限。[!UICONTROL Adobe Experience Cloud] 文档位于 [github.com](https://www.github.com/adobedocs) 上若干不同的存储库中。

1. 如果不确定要使用哪个存储库，请使用 Web 浏览器访问文章。选择文章右上角的 **Edit**（编辑）链接（铅笔图标）。（如果未看到“Edit”（编辑）链接，则表示该内容在 GitHub 中尚不可用。）

要对 Adobe 文档做出贡献，您可以通过克隆相应的文档存储库在本地创建和编辑 Markdown 文件。然后，使用拉取请求将更改合并到只读中央共享存储库中。

<!---
![GitHub Triangle](/assets/git-and-github-initial-setup.png)

If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]
-->

## 创建分支存储库

使用适当的存储库，使用 GitHub 网站在您自己的 GitHub 帐户中创建分支存储库。

由于所有主文档存储库都提供只读访问权限，这意味着您无法直接对存储库中的内容进行更改，因此需要使用个人分支存储库。要进行更改，您必须从分支存储库将拉取请求 (PR) 提交到主存储库。要实现此目的，首先您需要创建自己的存储库副本，以便具有写入权限。GitHub *分支存储库*&#x200B;可实现这一点。

1. 转到主存储库的 GitHub 页面，然后单击右上角的 **Fork**（创建分支）按钮。

   ![GitHub 分支存储库](assets/fork-simple.png)

1. 如果系统提示您，请选择 GitHub 帐户磁贴作为应创建分支的位置。此提示会在 GitHub 帐户中创建存储库的副本，称为分支。

1. 选择一个易于记忆和键入的文件夹名称。

   某些存储库可能较大。选择的位置应具有足够的可用磁盘空间。

   >[!NOTE]
   >
   >避免选择嵌套在另一个 git 存储库文件夹位置内的本地文件夹路径。尽管可以将 git 克隆文件夹存储在另一个文件夹旁边，但将 git 文件夹嵌套在另一个文件夹中会导致文件跟踪错误。

## 创建存储库的本地克隆

通过创建分支存储库的克隆，可以将文件的副本下载到计算机。准备就绪后，您可以将在本地驱动器上所作的编辑推送到服务器上的分支存储库。然后，您可以提交拉取请求以将上游存储库所做的编辑合并到主存储库中。

以下步骤假定您使用的是 GitHub Desktop。如果您使用的是其他客户端，则请进行适当调整。

1. 单击 **Clone or download**（克隆或下载），然后选择 **Open in Desktop**（在桌面中打开），以将存储库的副本（您的分支）拉到计算机的当前目录中。

   ![克隆存储库](assets/clone-pulldown.png)

1. 使用 GitHub Desktop 以将本地文件与分支存储库文件保持同步。

有关详细信息，请参阅 [GitHub Desktop 文档](https://help.github.com/desktop/)。
