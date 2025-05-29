---
title: ChartSeriesGroup.AxisGroup
linktitle: AxisGroup
articleTitle: AxisGroup
second_title: Aspose.Words for .NET
description: 发现 ChartSeriesGroup AxisGroup 属性，轻松管理系列组的轴，以增强数据可视化和分析。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/axisgroup/
---
## ChartSeriesGroup.AxisGroup property

获取或设置此系列组所属的轴组。

```csharp
public AxisGroup AxisGroup { get; set; }
```

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

* enum [AxisGroup](../../axisgroup/)
* class [ChartSeriesGroup](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
