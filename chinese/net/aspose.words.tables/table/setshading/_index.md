---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words for .NET
description: 使用 SetShading 方法增强表格的外观，允许您应用自定义阴影值以获得精致、专业的外观。
type: docs
weight: 450
url: /zh/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

将整个表格的阴影设置为指定值。

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| texture | TextureIndex | 要应用的纹理。 |
| foregroundColor | Color | 纹理的颜色。 |
| backgroundColor | Color | 背景填充的颜色。 |

## 例子

展示如何将外框应用于表格。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将表格与页面中心对齐。
table.Alignment = TableAlignment.Center;

// 清除表格中所有现有的边框和阴影。
table.ClearBorders();
table.ClearShading();

// 为表格轮廓添加绿色边框。
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// 用浅绿色纯色填充单元格。
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### 也可以看看

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
