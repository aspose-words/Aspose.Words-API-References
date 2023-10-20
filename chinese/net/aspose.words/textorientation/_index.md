---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.TextOrientation 枚举. 指定页面上表格单元格或文本框架中文本的方向 在 C#.
type: docs
weight: 6430
url: /zh/net/aspose.words/textorientation/
---
## TextOrientation enumeration

指定页面上、表格单元格或文本框架中文本的方向。

```csharp
public enum TextOrientation
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Horizontal | `0` | 文本水平排列 (lr-tb)。 |
| Downward | `1` | 文本向右旋转 90 度，从上到下显示 (tb-rl)。 |
| Upward | `3` | 文本向左旋转 90 度，从下到上显示 (bt-lr)。 |
| HorizontalRotatedFarEast | `4` | 文本水平排列，但远东字符向左旋转 90 度 (lr-tb-v)。 |
| VerticalFarEast | `5` | 远东字符垂直显示，其他文本向右旋转 90 度 以从上到下显示 (tb-rl-v)。 |
| VerticalRotatedFarEast | `7` | 远东字符垂直显示，其他文本向右旋转 90 度 以从上到下垂直显示，然后从左到右水平显示 (tb-lr-v)。 |

## 例子

演示如何构建格式化的 2x2 表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// 构建表时，文档构建器将应用其当前的 RowFormat/CellFormat 属性值
// 到其光标所在的当前行/单元格以及创建它们时的任何新行/单元格。
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// 先前添加的行和单元格不会受到构建器格式更改的影响。
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
