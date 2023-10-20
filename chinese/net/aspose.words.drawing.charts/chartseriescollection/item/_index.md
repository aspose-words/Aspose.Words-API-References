---
title: ChartSeriesCollection.Item
linktitle: Item
articleTitle: Item
second_title: 用于 .NET 的 Aspose.Words
description: ChartSeriesCollection Item 财产. 返回一个ChartSeries在指定的索引处 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

返回一个[`ChartSeries`](../../chartseries/)在指定的索引处。

```csharp
public ChartSeries this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合中的索引。 |

## 评论

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

## 例子

显示如何在图表中添加和删除系列数据。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个柱形图，默认包含三个系列的演示数据。
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// 每个系列有四个十进制值：四个类别中的每一个。
// 三列的四个集群将代表此数据。
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
// 这个图表现在将包含四个四列的集群。
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });

// 图表系列也可以通过索引移除，就像这样。
// 这将删除图表随附的三个演示系列之一。
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));

// 我们也可以用这个方法一次性清除所有图表的数据。
// 创建新图表时，这是擦除所有演示数据的方法
// 在我们开始处理空白图表之前。
chartData.Clear();
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
