---
title: ChartDataLabelCollection.Separator
second_title: Aspose.Words for .NET API 参考
description: ChartDataLabelCollection 财产. 获取或设置用于整个系列的数据标签的字符串分隔符 默认为逗号但饼图仅显示类别名称和百分比时除外此时应使用换行符 
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

获取或设置用于整个系列的数据标签的字符串分隔符。 默认为逗号，但饼图仅显示类别名称和百分比时除外，此时应使用换行符 。

```csharp
public string Separator { get; set; }
```

### 评论

可以使用 the 覆盖单个数据标签为此属性定义的值[`Separator`](../../chartdatalabel/separator/)属性.

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

展示如何使用饼图的数据标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 插入自定义图表系列，其中包含每个部门的类别名称及其频率表。
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// 启用数据标签，显示每个扇区的百分比和频率，并修改其外观。
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### 也可以看看

* class [ChartDataLabelCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* 部件 [Aspose.Words](../../../)


