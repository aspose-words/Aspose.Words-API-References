---
title: Table.CellSpacing
linktitle: CellSpacing
articleTitle: CellSpacing
second_title: Aspose.Words for .NET
description: 探索表格 CellSpacing 属性，轻松自定义单元格间距（以点为单位），增强表格的外观和可读性。
type: docs
weight: 100
url: /zh/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

获取或设置单元格之间的空间量（以点为单位）。

```csharp
public double CellSpacing { get; set; }
```

## 例子

展示如何在表格中启用各个单元格之间的间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// 将“AllowCellSpacing”属性设置为“true”以启用单元格之间的间距
// 其大小等于“CellSpacing”属性的值，以点为单位。
// 将“AllowCellSpacing”属性设置为“false”以禁用单元格间距
// 并忽略“CellSpacing”属性的值。
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// 调整“CellSpacing”属性将自动启用单元格间距。
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

展示如何为表格创建自定义样式设置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// 设置表格的样式属性可能会影响表格本身的属性。
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
