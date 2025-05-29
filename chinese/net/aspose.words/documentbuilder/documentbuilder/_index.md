---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 轻松创建功能强大的文档。立即初始化新实例，简化您的文档管理！
type: docs
weight: 10
url: /zh/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

初始化此类的新实例。

```csharp
public DocumentBuilder()
```

## 评论

创建新的[`DocumentBuilder`](../)对象并将其附加到新的[`Document`](../../document/)对象.

## 例子

展示如何使用 DocumentBuilder 插入格式化文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定字体格式，然后添加文本。
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

初始化此类的新实例。

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## 评论

创建新的[`DocumentBuilder`](../)对象并将其附加到新的[`Document`](../../document/)对象。 可以指定其他文档构建选项。

## 例子

展示如何忽略表格内容的格式。

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// 在表格前添加内容。
// 默认字体大小为 12。
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// 更改表格内的字体大小。
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// 如果 ContextTableFormatting 为真，则表格格式不会应用于之后的内容。
// 如果 ContextTableFormatting 为 false，则表格格式将应用于之后的内容。
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### 也可以看看

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

初始化此类的新实例。

```csharp
public DocumentBuilder(Document doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | Document | 这[`Document`](../../document/)要附加到的对象。 |

## 评论

创建新的[`DocumentBuilder`](../)对象，附加到指定的[`Document`](../../document/)对象。 光标位于文档开头。

## 例子

展示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望第一页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建页眉，然后向文档添加三页以显示每种页眉类型。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

展示如何使用标题样式作为条目将目录 (TOC) 插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入文档第一页的目录。
// 配置表格以选取标题级别为 1 至 3 的段落。
// 另外，将其条目设置为超链接，以便
// 在 Microsoft Word 中单击鼠标左键时移动到标题的位置。
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// 通过添加具有标题样式的段落来填充目录。
// 每个级别在 1 到 3 之间的标题都会在表中创建一个条目。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// 目录是一种需要更新以显示最新结果的字段。
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### 也可以看看

* class [Document](../../document/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

初始化此类的新实例。

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | Document | 这[`Document`](../../document/)要附加到的对象。 |
| options | DocumentBuilderOptions | 文档构建过程的附加选项。 |

## 评论

创建新的[`DocumentBuilder`](../)对象，附加到指定的[`Document`](../../document/)对象。 光标位于文档开头。

## 例子

展示如何忽略表格内容的格式。

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// 在表格前添加内容。
// 默认字体大小为 12。
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// 更改表格内的字体大小。
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// 如果 ContextTableFormatting 为真，则表格格式不会应用于之后的内容。
// 如果 ContextTableFormatting 为 false，则表格格式将应用于之后的内容。
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### 也可以看看

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
