---
title: Table.AbsoluteHorizontalDistance
linktitle: AbsoluteHorizontalDistance
articleTitle: AbsoluteHorizontalDistance
second_title: 用于 .NET 的 Aspose.Words
description: Table AbsoluteHorizontalDistance 财产. 获取或设置由表属性指定的绝对水平浮动表位置以点为单位 默认值为 0 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.tables/table/absolutehorizontaldistance/
---
## Table.AbsoluteHorizontalDistance property

获取或设置由表属性指定的绝对水平浮动表位置，以点为单位。 默认值为 0。

```csharp
public double AbsoluteHorizontalDistance { get; set; }
```

## 例子

显示如何设置浮动表的位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// 将表格的位置设置为页面上的某个位置，例如本例中的右下角。
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // 我们还可以设置距插入表格的段落位置的水平和垂直偏移（以磅为单位）。
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
