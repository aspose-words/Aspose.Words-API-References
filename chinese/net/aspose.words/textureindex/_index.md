---
title: TextureIndex Enum
linktitle: TextureIndex
articleTitle: TextureIndex
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TextureIndex 枚举，获取高级阴影纹理。使用可自定义的高质量纹理增强您的文档设计。
type: docs
weight: 7300
url: /zh/net/aspose.words/textureindex/
---
## TextureIndex enumeration

指定阴影纹理。

```csharp
public enum TextureIndex
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Texture10Percent | `3` |  |
| Texture12Pt5Percent | `37` |  |
| Texture15Percent | `38` |  |
| Texture17Pt5Percent | `39` |  |
| Texture20Percent | `4` |  |
| Texture22Pt5Percent | `40` |  |
| Texture25Percent | `5` |  |
| Texture27Pt5Percent | `41` |  |
| Texture2Pt5Percent | `35` |  |
| Texture30Percent | `6` |  |
| Texture32Pt5Percent | `42` |  |
| Texture35Percent | `43` |  |
| Texture37Pt5Percent | `44` |  |
| Texture40Percent | `7` |  |
| Texture42Pt5Percent | `45` |  |
| Texture45Percent | `46` |  |
| Texture47Pt5Percent | `47` |  |
| Texture50Percent | `8` |  |
| Texture52Pt5Percent | `48` |  |
| Texture55Percent | `49` |  |
| Texture57Pt5Percent | `50` |  |
| Texture5Percent | `2` |  |
| Texture60Percent | `9` |  |
| Texture62Pt5Percent | `51` |  |
| Texture65Percent | `52` |  |
| Texture67Pt5Percent | `53` |  |
| Texture70Percent | `10` |  |
| Texture72Pt5Percent | `54` |  |
| Texture75Percent | `11` |  |
| Texture77Pt5Percent | `55` |  |
| Texture7Pt5Percent | `36` |  |
| Texture80Percent | `12` |  |
| Texture82Pt5Percent | `56` |  |
| Texture85Percent | `57` |  |
| Texture87Pt5Percent | `58` |  |
| Texture90Percent | `13` |  |
| Texture92Pt5Percent | `59` |  |
| Texture95Percent | `60` |  |
| Texture97Pt5Percent | `61` |  |
| TextureCross | `24` |  |
| TextureDarkCross | `18` |  |
| TextureDarkDiagonalCross | `19` |  |
| TextureDarkDiagonalDown | `16` |  |
| TextureDarkDiagonalUp | `17` |  |
| TextureDarkHorizontal | `14` |  |
| TextureDarkVertical | `15` |  |
| TextureDiagonalCross | `25` |  |
| TextureDiagonalDown | `22` |  |
| TextureDiagonalUp | `23` |  |
| TextureHorizontal | `20` |  |
| TextureNone | `0` |  |
| TextureSolid | `1` |  |
| TextureVertical | `21` |  |
| TextureNil | `65535` | 指定当前阴影区域不得使用任何图案 （即图案应完全填充背景颜色）。 |

## 例子

展示如何使用边框和阴影装饰文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
