---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DocumentBuilderOptions，通过可定制的功能增强您的文档创建，获得无缝的构建体验。
type: docs
weight: 670
url: /zh/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

允许为文档构建过程指定附加选项。

```csharp
public class DocumentBuilderOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | 如果应用于表格内容的格式不会影响其后内容的格式，则为 True。 默认值为`真的`. |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | 对应于 Microsoft Word 中的设计模式。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
