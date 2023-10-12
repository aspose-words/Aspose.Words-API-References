---
title: Class ChartLegend
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartLegend 班级. 表示图表图例属性
type: docs
weight: 720
url: /zh/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

表示图表图例属性。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartLegend
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | 返回父图表的所有系列和趋势线的图例条目的集合。 |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | 确定是否允许其他图表元素与图例重叠。 默认值为`错误的`. |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | 指定图例在图表上的位置。 默认值为Right. |

### 例子

演示如何编辑图表图例的外观。

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

// 通过允许其他图表元素（例如图表）与图例重叠，为它们提供更多空间。
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


