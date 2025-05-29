---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words for .NET
description: 探索表格文本换行属性，轻松管理表格中的文本流向。灵活的文本选项提升可读性和设计感！
type: docs
weight: 310
url: /zh/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

获取或设置`TextWrapping`对于表.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## 例子

展示如何使用表格文本换行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// 将“TextWrapping”属性设置为“TextWrapping.Around”以使表格在其周围环绕文本，
//并通过设置位置将其推入下面的段落中。
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### 也可以看看

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
