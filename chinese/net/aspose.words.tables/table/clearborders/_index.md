---
title: Table.ClearBorders
linktitle: ClearBorders
articleTitle: ClearBorders
second_title: 用于 .NET 的 Aspose.Words
description: Table ClearBorders 方法. 删除此表上的所有表格和单元格边框 在 C#.
type: docs
weight: 370
url: /zh/net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

删除此表上的所有表格和单元格边框。

```csharp
public void ClearBorders()
```

## 例子

演示如何将轮廓边框应用到表格。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将表格与页面中心对齐。
table.Alignment = TableAlignment.Center;

// 清除表格中任何现有的边框和阴影。
table.ClearBorders();
table.ClearShading();

// 将绿色边框添加到表格的轮廓。
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// 用浅绿色纯色填充单元格。
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

演示如何删除表格中的所有边框。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

// 修改上边框的颜色和粗细。
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// 清除表格中所有单元格的边框，然后保存文档。
table.ClearBorders();
doc.Save(ArtifactsDir + "Table.ClearBorders.docx");

// 重新打开文档后验证表属性的值。
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
