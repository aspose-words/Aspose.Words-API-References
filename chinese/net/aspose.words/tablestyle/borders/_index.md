---
title: TableStyle.Borders
linktitle: Borders
articleTitle: Borders
second_title: 用于 .NET 的 Aspose.Words
description: TableStyle Borders 财产. 获取样式的默认单元格边框的集合 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/tablestyle/borders/
---
## TableStyle.Borders property

获取样式的默认单元格边框的集合。

```csharp
public BorderCollection Borders { get; }
```

## 例子

演示如何为表格创建自定义样式设置。

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

* class [BorderCollection](../../bordercollection/)
* class [TableStyle](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
