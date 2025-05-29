---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: 探索 ChartLegend Position 属性，轻松自定义图表的图例位置，以增强清晰度和视觉吸引力。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

指定图表上图例的位置。

```csharp
public LegendPosition Position { get; set; }
```

## 评论

默认值为Right适用于 Word 2016 之前的图表和 Top用于 Word 2016 图表。

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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
