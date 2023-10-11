---
title: Table.BottomPadding
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 获取或设置要在单元格内容下方添加的空间量以磅为单位
type: docs
weight: 90
url: /zh/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

获取或设置要在单元格内容下方添加的空间量（以磅为单位）。

```csharp
public double BottomPadding { get; set; }
```

### 例子

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
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


