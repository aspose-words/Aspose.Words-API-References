---
title: Table.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: 用于 .NET 的 Aspose.Words
description: Table RightPadding 财产. 获取或设置要添加到单元格内容右侧的空间量以磅为单位 在 C#.
type: docs
weight: 250
url: /zh/net/aspose.words.tables/table/rightpadding/
---
## Table.RightPadding property

获取或设置要添加到单元格内容右侧的空间量（以磅为单位）。

```csharp
public double RightPadding { get; set; }
```

## 例子

展示如何在表格中配置内容填充。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // 对于表中的每个单元格，设置其内容与其每个边框之间的距离。
// 该表将通过换行文本来保持最小填充距离。
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
