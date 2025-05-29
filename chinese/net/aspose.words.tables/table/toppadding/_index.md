---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words for .NET
description: 发现 Table TopPadding 属性，轻松调整单元格内容上方点的空间，以增强布局控制并提高可读性。
type: docs
weight: 330
url: /zh/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

获取或设置在单元格内容上方添加的空间量（以点为单位）。

```csharp
public double TopPadding { get; set; }
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
