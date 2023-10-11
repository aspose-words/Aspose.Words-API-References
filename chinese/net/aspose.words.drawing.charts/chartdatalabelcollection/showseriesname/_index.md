---
title: ChartDataLabelCollection.ShowSeriesName
second_title: Aspose.Words for .NET API 参考
description: ChartDataLabelCollection 财产. 返回或设置一个布尔值以指示整个系列的数据标签的系列名称显示行为 真的显示系列名称错误的隐藏默认情况下错误的.
type: docs
weight: 130
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

返回或设置一个布尔值，以指示整个系列的数据标签的系列名称显示行为。 `真的`显示系列名称；`错误的`隐藏。默认情况下`错误的`.

```csharp
public bool ShowSeriesName { get; set; }
```

### 评论

可以使用 the 覆盖单个数据标签为此属性定义的值[`ShowSeriesName`](../../chartdatalabel/showseriesname/)属性.

### 例子

演示如何使用气泡图的数据标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 添加带有 X/Y 坐标和每个气泡直径的自定义系列。
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// 启用数据标签，然后修改其外观。
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

### 也可以看看

* class [ChartDataLabelCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* 部件 [Aspose.Words](../../../)


