---
title: ChartSeriesGroupCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 探索 ChartSeriesGroupCollection Add 方法，轻松添加新的系列组，增强数据可视化能力。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---
## ChartSeriesGroupCollection.Add method

将指定系列类型的新系列组添加到此集合。

```csharp
public ChartSeriesGroup Add(ChartSeriesType seriesType)
```

## 评论

组合图只能包含以下类型的系列组：面积图、条形图、柱形图、折线图、饼图、散点图、 雷达和股票类型（相应的 3D 系列类型除外）。

## 例子

展示如何使用图表的次轴。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// 删除默认生成的系列。
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// 创建一个额外的系列组，也是线类型。
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// 指定新系列组使用次坐标轴。
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// 隐藏次要 X 轴。
newSeriesGroup.AxisX.Hidden = true;
// 定义次要 Y 轴的标题。
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// 将系列添加到新的系列组。
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### 也可以看看

* class [ChartSeriesGroup](../../chartseriesgroup/)
* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroupCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
