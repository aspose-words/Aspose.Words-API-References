---
title: ChartDataLabelCollection.ShowCategoryName
second_title: Aspose.Words for .NET API 参考
description: ChartDataLabelCollection 财产. 允许指定是否为整个系列的数据标签显示类别名称 默认值为错误的.
type: docs
weight: 80
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

允许指定是否为整个系列的数据标签显示类别名称。 默认值为`错误的`.

```csharp
public bool ShowCategoryName { get; set; }
```

### 评论

可以使用 the 覆盖单个数据标签为此属性定义的值[`ShowCategoryName`](../../chartdatalabel/showcategoryname/)属性.

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


