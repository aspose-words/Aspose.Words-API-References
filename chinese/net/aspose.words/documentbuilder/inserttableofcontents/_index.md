---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertTableOfContents 方法. 将 TOC目录字段插入到文档中 在 C#.
type: docs
weight: 460
url: /zh/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

将 TOC（目录）字段插入到文档中。

```csharp
public Field InsertTableOfContents(string switches)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switches | String | TOC 字段切换。 |

## 评论

此方法将 TOC（目录）字段插入到文档 at 的当前位置。

Word 文档中的目录可以通过多种方式构建并使用多种选项进行格式化。 Microsoft Word 的表格构建和显示方式由字段开关控制。

指定开关的最简单方法是使用“插入”-&gt;“参考”-&gt;“索引和表格”菜单将 内容表插入并配置到Word 文档中， 然后打开域代码显示以查看开关。您可以在 Microsoft Word 中按 Alt+F9 打开或关闭域代码的显示。

例如，创建目录后，以下字段将 insert 到文档中：**{ 目录 \o "1-3" \h \z \u }** . 您可以复制**\o“1-3”\h\z\u**并将其用作开关参数。

注意`InsertTableOfContents`只会插入一个 TOC 字段，但 不会实际构建目录。当字段更新时，目录由 Microsoft Word 构建。

如果使用此方法插入目录，然后在 Microsoft Word 中打开 file ，您将看不到目录，因为 TOC 字段 尚未更新。

在 Microsoft Word 中，打开文档时不会自动更新字段 ，但您可以随时按 F9 更新文档中的字段。

## 例子

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
