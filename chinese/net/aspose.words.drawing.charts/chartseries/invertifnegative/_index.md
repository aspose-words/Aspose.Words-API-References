---
title: ChartSeries.InvertIfNegative
linktitle: InvertIfNegative
articleTitle: InvertIfNegative
second_title: Aspose.Words for .NET
description: 探索 ChartSeries 的 InvertIfNegative 属性。轻松自定义负值的颜色反转，提升您的数据可视化体验。
type: docs
weight: 80
url: /zh/net/aspose.words.drawing.charts/chartseries/invertifnegative/
---
## ChartSeries.InvertIfNegative property

指定当值为负时父元素是否应反转其颜色。

```csharp
public bool InvertIfNegative { get; set; }
```

## 例子

展示如何处理折线图上的数据点。

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

    // 平滑代表第一个数据系列的线。
    chart.Series[0].Smooth = true;

    // 验证当值为负时第一个系列的数据点不会反转其颜色。
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // 为了使图表看起来更清晰，我们可以单独清除格式。
    dataPoint.ClearFormat();

    // 我们还可以一次性剥离整个系列的数据点。
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

* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
