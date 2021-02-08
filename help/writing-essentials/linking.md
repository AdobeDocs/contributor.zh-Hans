---
lastModified: 2018-06-28T00:00:00Z
title: 在文档中使用链接
seo-title: 在 Adobe Git/Markdown 文档中使用链接
description: 本文就如何创建指向内容和图像的链接，提供了相关指导。
seo-description: 本文就如何创建指向 Adobe 文档内容和图像的链接，提供了相关指导。
translation-type: ht
source-git-commit: df6c4152df0c1ee87c9fc4ca22e36a3f13cb620b
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---


# 在文档中使用链接

本文介绍了如何在文档页面中使用超链接。根据各种不同的约定，将链接添加到 Markdown 中并非难事。链接可将用户指向同一页面中的内容，指向其他相邻页面，或指向外部网站和 URL。

>[!IMPORTANT]
>理想情况下，只要目标支持（绝大情况下都应该支持），所有链接都应该是安全的链接（`https` 与 `http`）。

## 链接到 URL

您在链接文本中包含的单词应该是您要链接页面的标题或特定的描述性文本。

**示例：**

- `For more information, see the [overview article](https://github.com/AdobeDocs/target.en/help/overview.md).`

- `For more details, see [Adobe Legal Concerns](https://www.adobe.com/legal).`

## 从一篇文章链接到另一篇文章

要创建从一篇文章到同一存储库中另一篇文章的内联链接，请使用以下链接语法：

- 目录中的文章链接到同一目录中的另一篇文章：

   `[link text](article-name.md)`

- 子目录中的文章链接到根目录中的文章：

   `[link text](../article-name.md)`

- 子目录的子目录中的文章链接到根目录中的文章：

   `[link text](../../article-name.md)`

- 根目录中的文章链接到子目录中的文章：

   `[link text](./directory/article-name.md)`

- 子目录中的文章链接到另一个子目录中的文章：

   `[link text](../directory/article-name.md)`

- 子目录的子目录中的文章链接到另一个子目录中的文章：

   `[link text](../../directory/article-name.md)`

## 链接到锚点

无需创建锚点。所有 H2 标题的锚点会在发布时自动生成。您只需要创建指向 H2 (##) 部分的链接即可。

- 链接到同一文章中的标题：

   `[link](#the-text-of-the-level2-section-separated-by-hyphens)`

   `[Link to anchors](#links-to-anchors)`

- 链接到同一子目录中另一篇文章中的锚点：

   `[link text](article-name.md#anchor-name)`

   `[Configure your profile](overview.md#getting-started)`

- 链接到另一个服务子目录中的锚点：

   `[link text](../directory/article-name.md#anchor-name)`

   `[Configure your profile](../overview.md#configure-your-profile)`

## 链接到图像

作为最佳做法，图像和文件存储在与链接到它的 Markdown 文件处于同一级别的 `assets` 目录中。

- 文章链接到 `assets` 子目录中的图像：

   `![alt text](assets/image-name.png)`

- 文章链接到 `assets/no-localize` 子目录中的图像：

   `![alt text](assets/no-localize/image-name.png)`
