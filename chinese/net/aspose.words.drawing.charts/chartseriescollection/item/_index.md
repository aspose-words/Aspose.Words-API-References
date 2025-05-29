---
title: ChartSeriesCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 访问 ChartSeriesCollection Item 属性，通过索引轻松检索 ChartSeries，增强您的数据可视化体验。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

返回[`ChartSeries`](../../chartseries/)在指定的索引处。

```csharp
public ChartSeries this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合的索引。 |

## 评论

该索引从零开始。

允许使用负索引，表示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负数并且其绝对值大于列表中的项目数，则返回空引用。

## 例子

展示如何在图表中添加和删除系列数据。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个柱形图，默认包含三组演示数据。
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// 每个系列有四个十进制值：四个类别各一个。
// 四个三列的集群将代表该数据。
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// 打印图表中每个系列的名称。
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// 这些是图表中类别的名称。
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// 我们可以为现有类别添加具有新值的系列。
// 此图表现在将包含四个集群，每个集群有四列。
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// 也可以通过索引删除图表系列，就像这样。
// 这将删除图表附带的三个演示系列之一。
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// 我们还可以使用此方法一次清除所有图表的数据。
// 创建新图表时，这是清除所有演示数据的方法
// 然后我们才能开始处理空白图表。
chartData.Clear();
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
