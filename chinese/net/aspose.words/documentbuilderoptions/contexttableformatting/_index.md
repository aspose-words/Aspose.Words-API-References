---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilderOptions 中的 ContextTableFormatting 属性。确保表格格式保持独立，从而提升文档的清晰度和风格。
type: docs
weight: 20
url: /zh/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

如果应用于表格内容的格式不会影响其后内容的格式，则为 True。 默认值为`真的`.

```csharp
public bool ContextTableFormatting { get; set; }
```

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

* class [DocumentBuilderOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
