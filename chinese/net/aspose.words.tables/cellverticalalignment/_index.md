---
title: CellVerticalAlignment Enum
linktitle: CellVerticalAlignment
articleTitle: CellVerticalAlignment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Tables.CellVerticalAlignment 枚举，实现表格单元格中文本的最佳对齐。轻松优化您的文档布局！
type: docs
weight: 7130
url: /zh/net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

指定表格单元格内文本的垂直对齐。

```csharp
public enum CellVerticalAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Top | `0` | 文本与单元格顶部对齐。 |
| Center | `1` | 文本在单元格中间对齐。 |
| Bottom | `2` | 文本与单元格底部对齐。 |

## 例子

展示如何构建格式化的 2x2 表。

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

// 在构建表格时，文档构建器将应用其当前的 RowFormat/CellFormat 属性值
// 到其光标所在的当前行/单元格以及它创建的任何新行/单元格。
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

// 先前添加的行和单元格不会因构建器格式的更改而受到追溯影响。
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)
