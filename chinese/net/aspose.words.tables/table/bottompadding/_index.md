---
title: Table.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words for .NET
description: 发现表格 BottomPadding 属性，轻松调整单元格内容下方的间距，以增强布局控制并提高视觉吸引力。
type: docs
weight: 90
url: /zh/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

获取或设置在单元格内容下方添加的空间量（以点为单位）。

```csharp
public double BottomPadding { get; set; }
```

## 例子

展示如何配置表格中的内容填充。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // 对于表格中的每个单元格，设置其内容与其每个边框之间的距离。
// 此表将通过换行文本来保持最小填充距离。
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
