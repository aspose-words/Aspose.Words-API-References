---
title: DocumentBuilder.DocumentBuilder
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 构造函数. 初始化此类的新实例
type: docs
weight: 10
url: /zh/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

初始化此类的新实例。

```csharp
public DocumentBuilder()
```

### 评论

创建一个新的[`DocumentBuilder`](../)对象并将其附加到新的[`Document`](../../document/)对象.

### 例子

演示如何使用 DocumentBuilder 插入格式化文本。

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
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## DocumentBuilder(Document) {#constructor_1}

初始化此类的新实例。

```csharp
public DocumentBuilder(Document doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | Document | 这[`Document`](../../document/)要附加到的对象。 |

### 评论

创建一个新的[`DocumentBuilder`](../)对象，附加到指定的[`Document`](../../document/)object. 光标位于文档的开头。

### 例子

演示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望首页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建标题，然后向文档添加三个页面以显示每种标题类型。
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

演示如何使用标题样式作为条目将目录 (TOC) 插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入文档第一页的目录。
// 配置表格以选取标题为 1 至 3 级的段落。
// 此外，将其条目设置为将带我们进入的超链接
// 在 Microsoft Word 中左键单击时标题的位置。
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// 通过添加带有标题样式的段落来填充目录。
// 每个级别在 1 到 3 之间的此类标题将在表中创建一个条目。
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

// 目录是需要更新以显示最新结果的类型的字段。
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### 也可以看看

* class [Document](../../document/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


