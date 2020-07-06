---
lastModified: 2018-06-28T00:00:00Z
title: 如何使用 Markdown 编写文档
seo-title: 如何使用 Markdown 编写 Adobe 文档
description: 本文介绍了用于编写文章的 Markdown 语言的基础知识和参考信息。
seo-description: 本文介绍了用于为 Adobe 文档编写文章的 Markdown 语言的基础知识和参考信息。
translation-type: tm+mt
source-git-commit: 46674c112935a2a98a12210db92129a1bc475c46
workflow-type: tm+mt
source-wordcount: '1377'
ht-degree: 100%

---


# 如何使用 Markdown 编写技术文档

Adobe 技术文档文章以名为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻量级标记语言编写，这种方式易于阅读且易于学习。

当我们在 GitHub 中存储 Adobe Docs 内容时，该内容可以使用名为 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 的 Markdown 版本，该版本提供了额外的功能，可满足常见的格式需求。此外，Adobe 还通过几种方式扩展了 Markdown，以支持某些与帮助相关的功能，如备注、提示和嵌入式视频。

## Markdown 基础知识

### 标题

要创建标题，请在行首使用井号 (#)：

```
   # This is level 1 (article title)
   ## This is level 2
   ### This is level 3
   #### This is level 4
   ##### This is level 5
```

### 基本文本

Markdown 中的段落不需要特殊语法。

要将文本格式设置为&#x200B;**粗体**，请用两个星号将文本括起来。要将文本格式设置为&#x200B;*斜体*，请用一个星号将文本括起来：

```markdown
    This text is **bold**.
    This text is *italic*.
    This text is both ***bold and italic***.
```

<!--
To format superscript (H<sub>2</sub>O) and subscript (e=mc<sup>2</sup>) text:

```markdown
This is subscript H<sub>2</sub>O and superscript e=mc<sup>2</sup>.
```
-->

要忽略 Markdown 格式字符，请在字符前添加 \：

```markdown
This is not \*italicized\* type.
```

### 编号列表和项目符号列表

要创建编号列表，请在行首使用 `1.` 或 `1)`，但不要在同一列表中同时使用这两种格式。您无需指定编号。GitHub 会为您完成此操作。

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

将显示为：

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

<!-- markdownlint-disable MD037 -->
要创建项目符号列表，请在行首使用 \* 或者 - 或 +，但不要在同一列表中混合使用这几种格式。（请勿在同一文档中混合使用项目符号格式，例如 \* 和 \+。）
<!-- markdownlint-disable MD037 -->

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

将显示为：

* First item in an unordered list.
* Another item.
* Here we go again.

您还可以在列表中嵌入列表并在列表项之间添加内容。

```markdown
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |  
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.
```

将显示为：

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

### 表格

虽然表格不是核心 Markdown 规范的一部分，但 Adobe 仍在一定程度上支持它们。Markdown 不支持在单元格中使用多个行列表。最佳做法是避免在表格中使用多个行。您可以通过使用管道 (|) 字符绘制列和行来创建表格。连字符用于创建每个列的标题，而管道符用于分隔每个列。在表格前面添加一个空白行，以便该表格可正确呈现。

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

将显示为：

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Markdown 中可轻松处理简单的表格。但是，如果表格单元格中包含多个段落或列表，就会很难处理。对于此类内容，我们建议使用不同的格式，例如标题和文本。

有关创建表格的详细信息，请参阅：

* GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)
* [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web 应用程序
* [将 HTML 表转换为 Markdown](https://jmalarcon.github.io/markdowntables/)

### 链接

内联链接的 Markdown 语法由 `[link text]` 部分 + `(file-name.md)` 部分组成，前部分是将被添加超链接的文本，后部分是链接到的 URL 或文件名：

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

将显示为：

[Adobe](https://www.adobe.com/cn)

对于指向存储库中文章（交叉引用）的链接，请使用相对链接。您可以使用所有相对链接操作数，例如 ./（当前目录）、../（上一级目录），以及 ../../（上二级目录）。

```markdown
See [Overview example article](../../overview.md)
```

有关链接的更多信息，请参阅本指南的[链接](linking.md)文章以了解链接语法。

### 图像

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

将显示为：

![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")

### 代码块

Markdown 支持在句子中置入内联代码块，以及用于分隔句子的“受防护”块。有关详细信息，请参阅 [Markdown 对代码块的本机支持](https://daringfireball.net/projects/markdown/syntax#precode)

使用重反撇号 (\`) 可在段落中创建内联代码样式。要创建特定的多行代码块，请在代码块前后添加三个反撇号 (\`\`\`)（在 Markdown 中称为“受防护的代码块”，在 AEM 中仅称为“代码块”组件）。对于受防护的代码块，在第一组反撇号之后添加代码语言，以便 Markdown 正确地高亮显示代码语法。示例：\`\`\`javascript

示例：

```markdown
This is `inline code` within a paragraph of text.
```

将显示为：

This is `inline code` within a paragraph of text.

这是一个受防护的代码块：

```markdown
\```javascript
function test() {
 console.log("notice the blank line before this function?");
\```
```

将显示为：

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

您可以指定代码块的属性以关闭行号（默认情况下为开启）或添加换行（默认情况下为关闭）。使用 {line-numbers=&quot;no&quot;} 和 {line-wrap=&quot;yes&quot;}。以下属性是自定义 Markdown 扩展。

\`\`\`javascript {line-numbers=&quot;no&quot;}
function test() {
console.log(&quot;notice the blank line before this function?&quot;);
\`\`\`

### 定义列表

定义列表是一个 Markdown 扩展，它支持 AEM 中的定义列表组件。定义列表包括术语及其定义。

<!--

```markdown
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

Displayed:

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
--->

#### 标注和注释

注释（标注）不会出现在面向公众的帮助文章中。但是，它会出现在用户可以查看和编辑的面向公众的 Markdown 文件中。

## 自定义 Markdown 扩展

Adobe 文章对大多数文章格式使用标准 Markdown，例如段落、链接、列表和标题。对于更丰富的格式，文章可以使用扩展的 Markdown 功能，例如：

* 备注块
* 嵌入式视频
* 不进行本地化
* 组件属性，例如为标题指定不同的标题 ID

在每行开头使用 Markdown 块引用 ( > ) 可将扩展组件（例如备注）绑定在一起。如果需要在组件中使用子组件，请为该子组件部分添加额外级别的块引用 (>  >)。例如，DONOTLOCALIZE 部分中的“备注”应以 >    > 开头。

一些常见的 Markdown 元素（如标题和代码块）包含扩展属性。如果需要更改默认属性，请将参数添加到组件后面的大括号 /{ /} 中。上下文中介绍了扩展属性。

### 备注块

您可以从四种类型的备注块中进行选择，以引起用户对特定内容的注意：

* `[!NOTE]`
* `[!CAUTION]`
* `[!TIP]`
* `[!IMPORTANT]`

通常，应谨慎使用备注块，因为它们可能具有破坏性。尽管它们也支持代码块、图像、列表和链接，但请尽量保持备注块简单、直观。


```markdown
>[!NOTE]
>
>This is a standard NOTE block.
```

将显示为：

>[!NOTE]
>
>This is a standard NOTE block.

```markdown
>[!TIP]
>
>This is a standard tip.
```

将显示为：

>[!TIP]
>
>This is a standard tip.

### 视频

嵌入式视频不会呈现在 Markdown 本地，但您可以使用此 Markdown 扩展。

```markdown
>[!VIDEO](https://www.youtube.com/watch?v=A0EcD2AxvJE)
```

将显示为：

>[!VIDEO](https://www.youtube.com/watch?v=A0EcD2AxvJE)

### 更多与此类似的内容

AEM 中的“更多与此类似的内容”组件显示在文章的末尾。此部分会显示相关链接。呈现文章时，可以将其格式化为与 2 级标题 (##) 相同的格式而不添加到 mini-TOC。

```markdown
>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

将显示为：

>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/cn/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/cn/support/audience-manager.html)


### DNL（不进行本地化）和 UICONTROL

在某些情况下，我们需要仅将文章中某些内容部分标记为英文。
需要向我们的翻译系统声明单词、短语和其他元素，并创建管理受控词典的功能。

对于不应进行本地化的单词或短语，请使用 `[!DNL]` 扩展来将单词或部分括起来。

对于解决方案的用户界面和菜单中的元素，我们使用 `` 扩展。

**示例：**

在 [!DNL Adobe Target] 中，您可以在支持 [!DNL Target] 的页面上直接创建测试。

**来源：**

```markdown
In [!DNL Adobe Target] you can create your tests directly on a [!DNL Target]-enabled page.
```

**示例**

在 [!DNL Target] 中使用 [!UICONTROL Visual Experience Composer]，可以在页面上直接创建测试。

**来源：**

```markdown
Use the [!UICONTROL Visual Experience Composer] in [!DNL Target] to create your test directly on a page.
```

## 难题和故障排除

### 替换文字

包含下划线的替换文字将无法正确呈现。例如，不要使用：

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

最佳做法是在文件名中使用连字符 (-)，而不是下划线 (_)。

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### 撇号和引号

如果将文本复制到 Markdown 编辑器，则文本可能包含“智能”（弯）撇号或引号。需要将这些符号编码或更改为基本撇号或单引号。否则，在发布文件时，最终将会得到这样的奇怪字符：Itâ€™s

以下是这些标点符号的“智能”版本的编码：

* 左（开）引号： `&#8220;`
* 右（闭）引号：`&#8221;`
* 右（闭）单引号或撇号：`&#8217;`
* 左（开）单引号（很少使用）：`&#8216;`

### 尖括号

如果在文件中的文本（而非代码）中使用尖括号（例如，表示占位符），则需要手动编码尖括号。否则，Markdown 会认为它们是一个 HTML 标记。

例如，将 `<script name>` 编码为 `&lt;script name&gt;`

### 标题中的与号

标题中不允许包含与号 (&amp;)。请改用“和”，或使用 `&amp;` 编码。

## 另请参阅

### Markdown 资源

* [Markdown 简介](https://daringfireball.net/projects/markdown/syntax)
* [GitHub 的 Markdown 基础知识](https://help.github.com/articles/markdown-basics/)
