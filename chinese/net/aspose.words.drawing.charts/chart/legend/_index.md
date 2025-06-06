---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words for .NET
description: 探索“图表图例”属性，轻松自定义图表。使用定制的图例选项增强数据可视化，获得更深入的洞察！
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

提供对图表图例属性的访问。

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
