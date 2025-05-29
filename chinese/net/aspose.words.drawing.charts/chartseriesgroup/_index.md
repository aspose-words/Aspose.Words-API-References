---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartSeriesGroup 类，它简化了图表系列属性的管理，从而增强了数据可视化和分析。
type: docs
weight: 1090
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

表示图表系列组的属性，即与相同轴关联的相同类型的图表系列的属性。

```csharp
public class ChartSeriesGroup
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | 获取或设置此系列组所属的轴组。 |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | 提供对该系列组 X 轴属性的访问。 |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | 提供对此系列组 Y 轴属性的访问。 |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | 获取或设置气泡的大小（以其默认大小的百分比表示）。 |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | 获取或设置父级圆环图的孔径大小（以百分比表示）。 |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | 获取或设置父饼图第一片的角度（以度为单位）。 |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | 获取或设置图表元素之间的间隙宽度百分比。 |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | 获取或设置系列条形或柱形重叠的百分比。 |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | 获取或设置饼图次要部分的大小（以百分比表示）。 |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | 获取属于此系列组的系列集合。 |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | 获取此组中包含的图表系列的类型。 |

## 评论

组合图表包含多个图表系列组，每个系列类型都有一个单独的组。

此外，您还可以创建图表系列组来将次坐标轴分配给一个或多个图表系列。

要了解更多信息，请访问[ 使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
