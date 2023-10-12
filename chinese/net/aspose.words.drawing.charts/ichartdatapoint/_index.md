---
title: Interface IChartDataPoint
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.IChartDataPoint 界面. 包含图表上单个数据点的属性
type: docs
weight: 900
url: /zh/net/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface

包含图表上单个数据点的属性。

```csharp
public interface IChartDataPoint
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/ichartdatapoint/bubble3d/) { get; set; } | 指定气泡图中的气泡是否应应用 3-D 效果。 |
| [Explosion](../../aspose.words.drawing.charts/ichartdatapoint/explosion/) { get; set; } | 指定数据点应从饼图中心移动的量。 可以为负数，负数表示未设置属性且不应应用爆炸。 仅适用于饼图。 |
| [InvertIfNegative](../../aspose.words.drawing.charts/ichartdatapoint/invertifnegative/) { get; set; } | 指定如果值为负数，父元素是否应反转其颜色。 |
| [Marker](../../aspose.words.drawing.charts/ichartdatapoint/marker/) { get; } | 指定数据标记。根据请求自动创建标记。 |

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


