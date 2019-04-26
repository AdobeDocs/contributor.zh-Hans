---
lastModified: '2018-06-28'
title: 在文档中使用链接
seo-title: 在 Adobe Git/Markdown 文档中使用链接
description: 本文就如何创建指向内容和图像的链接，提供了相关指导。
seo-description: 本文就如何创建指向 Adobe 文档内容和图像的链接，提供了相关指导。
translation-type: ht
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---


# 在文档中使用链接

本文介绍了如何在文档页面中使用超链接。根据各种不同的约定，将链接添加到 Markdown 中并非难事。链接可将用户指向同一页面中的内容，指向其他相邻页面，或指向外部网站和 URL。

> [!IMPORTANT]
> 理想情况下，只要目标支持（绝大情况下都应该支持），所有链接都应该是安全的链接（`https` 与 `http`）。

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

<!--
## Bob's link test

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> File Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>A comma-separated values file (such as one created in Excel). This is the file that contains the customer attribute data. See [Link TEST](/help/setup/full-workflow.md) </p> <p> <b>Naming requirements:</b> Ensure that file name extensions do not contain white spaces. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Required) The <span class="filepath"> .fin </span> file tells the system that you are finished uploading data. The name of the <span class="filepath"> .fin </span> file must match the name of the <span class="filepath"> .csv </span> file. </p> <p>Adobe recommends creating an empty text file with a <span class="filepath"> .fin </span> extension. An empty file saves space and upload time. </p> <p> <p>Note:  Renaming a <span class="filepath"> .fin </span> file is not allowed after it is uploaded. The <span class="filepath"> .fin </span> file must be uploaded separately and cannot be a renamed, previously uploaded file. </p> </p> <p>After you upload the <span class="filepath"> .fin </span> file in the customer attributes FTP, the system retrieves data quickly (within one minute). This differs from other Adobe FTP-based systems, which pick up data less frequently (around once per hour). </p> <p>The <span class="filepath"> .fin </span> file is not required when using the drag-and-drop upload method. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz </span> or <span class="filepath"> .zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz </span> (gzip) or <span class="filepath"> .zip </span> - for compressed files. A <span class="filepath"> .zip </span> file cannot contain more than one file in the archive. </p> <p> <b>Naming requirements:</b> The name of the <span class="filepath"> .zip </span> or <span class="filepath"> .gz </span> should match the name of the <span class="filepath"> .csv </span>. For example, if your <span class="filepath"> .csv </span> file is <span class="filepath"> crm_small.csv </span>, the <span class="filepath"> .zip </span> file should be <span class="filepath"> crm_small.csv.zip </span>. </p> <p>The .fin file must match the .csv. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->
