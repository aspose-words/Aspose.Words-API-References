---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words for .NET
description: 探索单元格 LastParagraph 属性。轻松从直接子元素访问最后一段，实现高效的内容管理。
type: docs
weight: 60
url: /zh/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

获取直接子段落中的最后一段。

```csharp
public Paragraph LastParagraph { get; }
```

## 例子

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
