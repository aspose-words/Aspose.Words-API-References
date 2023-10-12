---
title: Class ChartDataPoint
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartDataPoint 班级. 允许指定图表上单个数据点的格式
type: docs
weight: 690
url: /zh/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

允许指定图表上单个数据点的格式。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartDataPoint : IChartDataPoint
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | 指定气泡图中的气泡是否应应用 3-D 效果。 |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | 指定数据点应从饼图中心移动的量。 可以为负数，负数表示未设置属性且不应应用爆炸。 仅适用于饼图。 |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | 提供对此数据点的填充和线条格式的访问。 |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | 该对象应用格式的数据点的索引。 |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | 指定如果值为负数，父元素是否应反转其颜色。 |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | 指定图表数据标记。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | 清除该数据点的格式。属性设置为父系列中定义的默认值。 |

### 评论

在一个系列中，`ChartDataPoint`对象是一个成员[`ChartDataPointCollection`](../chartdatapointcollection/)。 的[`ChartDataPointCollection`](../chartdatapointcollection/)包含一个`ChartDataPoint`每个点的对象。

### 例子

展示如何使用折线图上的数据点。

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // 通过使图表的数据点显示为菱形来强调它们。
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // 平滑表示第一个数据系列的线。
    chart.Series[0].Smooth = true;

    // 验证如果值为负数，第一个系列的数据点不会反转其颜色。
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // 为了使图表看起来更清晰，我们可以单独清除格式。
    chart.Series[1].DataPoints[2].ClearFormat();

    // 我们还可以一次剥离整个系列的数据点。
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// 将多个数据点应用于一个系列。
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### 也可以看看

* interface [IChartDataPoint](../ichartdatapoint/)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


