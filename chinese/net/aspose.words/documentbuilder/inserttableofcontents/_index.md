---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder InsertTableOfContents 方法轻松增强您的文档，添加动态目录以便于导航和改善组织。
type: docs
weight: 500
url: /zh/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

将 TOC（目录）字段插入文档。

```csharp
public Field InsertTableOfContents(string switches)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switches | String | TOC 字段切换。 |

## 评论

此方法将 TOC（内容表）字段插入到文档的当前位置 at 中。

Word 文档中的目录可以通过多种方式创建，并使用各种选项进行格式化。Microsoft Word 中目录的创建和显示方式由字段开关控制。

指定开关最简单的方法是使用“插入”-&gt;“引用”-&gt;“索引和目录”菜单，在 Word 文档中插入并配置目录，然后打开“字段代码显示”即可查看开关。您可以在 Microsoft Word 中按 Alt+F9 来打开或关闭“字段代码显示”。

例如，创建目录后，将以下字段插入到文档中：**{ 目录 \o "1-3" \h \z \u }** . 您可以复制**\o "1-3" \h \z \u**并将其用作开关参数。

注意`InsertTableOfContents`只会插入目录字段，但 不会真正构建目录。目录是由 Microsoft Word 在字段更新时构建的。

如果您使用此方法插入目录，然后在 Microsoft Word 中打开文件 ，您将看不到目录，因为 TOC 字段 尚未更新。

在 Microsoft Word 中，打开文档时字段不会自动更新， 但您可以随时按 F9 来更新文档中的字段。

## 例子

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
