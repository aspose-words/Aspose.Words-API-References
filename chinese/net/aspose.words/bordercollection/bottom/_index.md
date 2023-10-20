---
title: BorderCollection.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: 用于 .NET 的 Aspose.Words
description: BorderCollection Bottom 财产. 获取底部边框 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

获取底部边框。

```csharp
public Border Bottom { get; }
```

## 例子

展示如何在构建表格时应用边框和底纹颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启动一个表格并为其边框设置默认颜色/厚度。
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// 创建一个包含两个具有不同背景颜色的单元格的行。
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

* class [Border](../../border/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
