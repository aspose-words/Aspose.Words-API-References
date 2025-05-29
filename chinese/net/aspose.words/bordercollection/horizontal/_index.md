---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words for .NET
description: 探索 BorderCollection 的“水平”属性，实现单元格和段落的无缝边框。通过完美的对齐和样式，提升您的布局！
type: docs
weight: 50
url: /zh/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

获取单元格或符合段落之间使用的水平边框。

```csharp
public Border Horizontal { get; }
```

## 例子

展示如何将水平边框设置应用于段落格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为段落创建红色水平边框。之后创建的任何段落都将继承这些边框设置。
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// 将文本写入文档，而不创建新的段落。
// 由于下方没有段落，因此水平边框将不可见。
builder.Write("Paragraph above horizontal border.");

// 一旦我们添加第二个段落，第一个段落的边框就会变得可见。
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

展示如何将垂直边框设置应用于表格行的格式。

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

    // 调整行间边框的外观。
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // 调整单元格之间边框的外观。
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
