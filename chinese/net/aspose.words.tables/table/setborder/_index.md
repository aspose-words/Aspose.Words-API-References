---
title: Table.SetBorder
second_title: Aspose.Words for .NET API 参考
description: Table 方法. 将指定的表格边框设置为指定的线条样式宽度和颜色
type: docs
weight: 430
url: /zh/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

将指定的表格边框设置为指定的线条样式、宽度和颜色。

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| borderType | BorderType | 要更改的表格边框。 |
| lineStyle | LineStyle | 要应用的线条样式。 |
| lineWidth | Double | 要设置的线宽（以磅为单位）。 |
| color | Color | 用于边框的颜色。 |
| isOverrideCellBorders | Boolean | 什么时候`真的`，导致所有现有的显式单元格边框被删除。 |

### 例子

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

### 也可以看看

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


