---
title: Table.RelativeVerticalAlignment
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 获取或设置浮动表相对垂直对齐方式
type: docs
weight: 240
url: /zh/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

获取或设置浮动表相对垂直对齐方式。

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
```

### 例子

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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


