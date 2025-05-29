---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.PresetTexture 枚举，使用可自定义的纹理增强您的形状，从而获得令人惊叹的文档设计。
type: docs
weight: 1560
url: /zh/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

指定用于填充形状的纹理。

```csharp
public enum PresetTexture
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `-1` | 无纹理。 |
| BlueTissuePaper | `1` | 蓝色薄纸纹理。 |
| Bouquet | `2` | 花束纹理。 |
| BrownMarble | `3` | 棕色大理石纹理。 |
| Canvas | `4` | 画布纹理。 |
| Cork | `5` | 软木纹理。 |
| Denim | `6` | 牛仔布纹理。 |
| FishFossil | `7` | 鱼化石纹理。 |
| Granite | `8` | 花岗岩纹理。 |
| GreenMarble | `9` | 绿色大理石纹理。 |
| MediumWood | `10` | 中等木质纹理。 |
| Newsprint | `11` | 新闻纸纹理。 |
| Oak | `12` | 橡木纹理。 |
| PaperBag | `13` | 纸袋纹理。 |
| Papyrus | `14` | 纸莎草纹理。 |
| Parchment | `15` | 羊皮纸纹理。 |
| PinkTissuePaper | `16` | 粉色薄纸纹理。 |
| PurpleMesh | `17` | 紫色网格纹理。 |
| RecycledPaper | `18` | 再生纸纹理。 |
| Sand | `19` | 沙子纹理。 |
| Stationery | `20` | 文具纹理。 |
| Walnut | `21` | 胡桃木纹理。 |
| WaterDroplets | `22` | 水滴纹理。 |
| WhiteMarble | `23` | 白色大理石纹理。 |
| WovenMat | `24` | 编织垫纹理。 |

## 例子

展示如何设置标记格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// 删除默认生成的系列。
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// 设置标记格式。
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
