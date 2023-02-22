---
title: ChartDataLabelCollection.ShowBubbleSize
second_title: Aspose.Words for .NET API 参考
description: ChartDataLabelCollection 财产. 允许指定是否为整个系列的数据标签显示气泡大小 仅适用于气泡图 默认值为 错误的.
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/
---
## ChartDataLabelCollection.ShowBubbleSize property

允许指定是否为整个系列的数据标签显示气泡大小。 仅适用于气泡图。 默认值为 **错误的**.

```csharp
public bool ShowBubbleSize { get; set; }
```

### 评论

可以使用 为单个数据标签覆盖为此属性定义的值[`ShowBubbleSize`](../../chartdatalabel/showbubblesize/)属性.

### 例子

展示如何使用气泡图的数据标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

 // 添加一个自定义系列，其中包含每个气泡的 X/Y 坐标和直径。
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// 启用数据标签，然后修改它们的外观。
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


