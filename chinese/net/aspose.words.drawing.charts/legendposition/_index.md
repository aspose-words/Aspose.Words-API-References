---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.LegendPosition 枚举，轻松自定义图表图例的位置，以增强数据可视化。
type: docs
weight: 1230
url: /zh/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

指定图表图例的可能位置。

```csharp
public enum LegendPosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 图表不会显示图例。 |
| Bottom | `1` | 指定图例应绘制在图表底部。 |
| Left | `2` | 指定图例应绘制在图表的左侧。 |
| Right | `3` | 指定图例应绘制在图表的右侧。 |
| Top | `4` | 指定图例应绘制在图表顶部。 |
| TopRight | `5` | 指定图例应绘制在图表的右上角。 |

## 例子

展示如何编辑图表图例的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// 将图表的图例移动到右上角。
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// 允许其他图表元素（例如图形）与图例重叠，从而为它们提供更多空间。
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
