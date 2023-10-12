---
title: TableStyle.Shading
second_title: Aspose.Words for .NET API 参考
description: TableStyle 财产. 获得Shading引用表格单元格的底纹格式的对象
type: docs
weight: 130
url: /zh/net/aspose.words/tablestyle/shading/
---
## TableStyle.Shading property

获得[`Shading`](../../shading/)引用表格单元格的底纹格式的对象。

```csharp
public Shading Shading { get; }
```

### 例子

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

* class [Shading](../../shading/)
* class [TableStyle](../)
* 命名空间 [Aspose.Words](../../tablestyle/)
* 部件 [Aspose.Words](../../../)


