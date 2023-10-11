---
title: BorderCollection.Horizontal
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 财产. 获取在单元格或一致段落之间使用的水平边框
type: docs
weight: 50
url: /zh/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

获取在单元格或一致段落之间使用的水平边框。

```csharp
public Border Horizontal { get; }
```

### 例子

演示如何将水平边框设置应用到段落格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为段落创建红色水平边框。之后创建的任何段落都将继承这些边框设置。
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// 将文本写入文档，之后不创建新段落。
// 由于下面没有段落，因此水平边框将不可见。
builder.Write("Paragraph above horizontal border.");

// 一旦我们添加第二个段落，第一个段落的边框将变得可见。
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

演示如何将垂直边框设置应用到表格行的格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个具有红色和蓝色内边框的表格。
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // 调整行之间出现的边框的外观。
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // 调整单元格之间出现的边框的外观。
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// 行格式和单元格的内部段落使用不同的边框设置。
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### 也可以看看

* class [Border](../../border/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


