---
title: ChartSeriesCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: 用于 .NET 的 Aspose.Words
description: ChartSeriesCollection RemoveAt 方法. 删除一个ChartSeries在指定的索引处 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chartseriescollection/removeat/
---
## ChartSeriesCollection.RemoveAt method

删除一个[`ChartSeries`](../../chartseries/)在指定的索引处。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 从零开始的索引[`ChartSeries`](../../chartseries/)去除。 |

## 例子

演示如何在图表中添加和删除系列数据。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个柱形图，默认包含三个系列的演示数据。
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// 每个系列都有四个十进制值：四个类别中的每一个都有一个。
// 三列的四个簇将代表此数据。
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
// 此图表现在将包含四个簇（每簇四列）。
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// 图表系列也可以通过索引删除，就像这样。
// 这将删除图表附带的三个演示系列之一。
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// 我们也可以用这个方法一次性清除所有图表的数据。
// 创建新图表时，这是擦除所有演示数据的方法
// 在我们开始处理空白图表之前。
chartData.Clear();
```

### 也可以看看

* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
