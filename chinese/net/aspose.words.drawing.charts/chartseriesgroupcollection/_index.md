---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChartSeriesGroupCollection 类，这是您轻松管理和组织 ChartSeriesGroup 对象的首选解决方案。
type: docs
weight: 1100
url: /zh/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

代表[`ChartSeriesGroup`](../chartseriesgroup/)对象.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | 返回此集合中的系列组数。 |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | 返回[`ChartSeriesGroup`](../chartseriesgroup/)在指定的索引处。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | 将指定系列类型的新系列组添加到此集合。 |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | 返回一个枚举器对象。 |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | 移除指定索引处的系列组。所有子系列都将从图表中移除。 |

## 评论

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/) 文档文章.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
