---
title: Table.ClearShading
second_title: Aspose.Words for .NET API 参考
description: Table 方法. 移除桌子上的所有阴影
type: docs
weight: 380
url: /zh/net/aspose.words.tables/table/clearshading/
---
## Table.ClearShading method

移除桌子上的所有阴影。

```csharp
public void ClearShading()
```

### 例子

显示如何将轮廓边框应用于表格。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将表格与页面中心对齐。
table.Alignment = TableAlignment.Center;

// 清除表格中任何现有的边框和阴影。
table.ClearBorders();
table.ClearShading();

// 为表格的轮廓添加绿色边框。
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// 用浅绿色纯色填充单元格。
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


