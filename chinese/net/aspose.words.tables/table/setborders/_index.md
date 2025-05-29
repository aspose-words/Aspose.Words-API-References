---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words for .NET
description: 使用 SetBorders 方法轻松自定义您的表格，调整线条样式、宽度和颜色以获得精致、专业的外观。
type: docs
weight: 440
url: /zh/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

将所有表格边框设置为指定的线条样式、宽度和颜色。

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| lineStyle | LineStyle | 要应用的线条样式。 |
| lineWidth | Double | 要设置的线宽（以点为单位）。 |
| color | Color | 边框使用的颜色。 |

## 例子

展示如何一次性格式化表格的所有边框。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 清除表中的所有现有边框。
table.ClearBorders();

// 设置一条绿线作为此表的每个外边框和内边框。
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

展示如何在构建表格时应用边框和阴影颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启动一个表格并设置其边框的默认颜色/粗细。
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// 创建一行包含两个具有不同背景颜色的单元格。
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// 重置单元格格式以禁用背景颜色
// 为构建器创建的所有新单元格设置自定义边框粗细，
// 然后构建第二行。
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### 也可以看看

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
