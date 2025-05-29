---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words for .NET
description: 在 Aspose.Words 中应用预定义的图表样式。使用 ChartStyle 枚举增强视觉效果，实现专业的文档格式。
type: docs
weight: 1130
url: /zh/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

指定图表的预定义样式。

```csharp
public enum ChartStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Normal | `0` | 表示默认图表样式。 |
| Muted | `1` | 色彩柔和的风格。 |
| Saturated | `2` | 色彩更饱和的风格。 |
| Shaded | `3` | 带有阴影数据点的样式。 |
| Flat | `4` | 具有平坦数据点且无渐变的样式。 |
| Shadowed | `5` | 数据点带有阴影的样式。 |
| Gradient | `6` | 数据点渐变填充样式。 |
| Original | `7` | 具有图表原始外观的样式。 |
| Transparent1 | `8` | 具有透明数据点的样式。 |
| Transparent2 | `9` | 具有透明数据点的样式。 |
| Outline | `10` | 数据点没有填充，只有轮廓的样式。 |
| OutlineBlack | `11` | 具有黑色图表背景的样式，其中数据点没有填充，只有轮廓。 |
| Black | `12` | 具有黑色图表背景的样式。 |
| Grey | `13` | 具有灰色渐变图表背景的样式。 |
| Blue | `14` | 具有蓝色图表背景的样式。 |
| ShadedPlot | `15` | 样式，其中绘图区域为阴影。 |

## 例子

展示如何设置和获取图表样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入黑色样式的图表。
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// 获取要更新的图表。
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// 获取图表样式。
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
