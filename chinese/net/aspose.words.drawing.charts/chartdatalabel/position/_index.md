---
title: ChartDataLabel.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: 探索 ChartDataLabel Position 属性，轻松自定义数据标签的位置，以增强数据可视化和清晰度。
type: docs
weight: 100
url: /zh/net/aspose.words.drawing.charts/chartdatalabel/position/
---
## ChartDataLabel.Position property

获取或设置数据标签的位置。

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## 评论

可以为以下图表系列类型的数据标签设置位置：

-Bar，Column , Histogram，Pareto , Waterfall ；允许值：Center , InsideBase，InsideEndand OutsideEnd；

-BarStacked，BarPercentStacked , ColumnStacked，ColumnPercentStacked ；允许的 值：Center，InsideBase 和InsideEnd；

-Bubble，Bubble3D , Line，LineStacked , LinePercentStacked，Scatter , Stock ；允许值：Center , Left，Right , Above和Below；

-Pie，Pie3D , PieOfBar，PieOfPie ；允许值： Center，InsideEnd , OutsideEnd和BestFit；

-BoxAndWhisker ；允许值： Left，Right , Above和Below。

## 例子

显示如何设置数据标签的位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入柱状图。
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// 删除默认生成的系列。
seriesColl.Clear();

// 添加系列。
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// 显示数据标签并设置字体颜色。
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// 设置数据标签位置。
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### 也可以看看

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabel](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
