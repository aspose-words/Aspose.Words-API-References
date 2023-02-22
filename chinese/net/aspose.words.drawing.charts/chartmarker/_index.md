---
title: Class ChartMarker
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartMarker 班级. 表示图表数据标记
type: docs
weight: 710
url: /zh/net/aspose.words.drawing.charts/chartmarker/
---
## ChartMarker class

表示图表数据标记。

```csharp
public class ChartMarker
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Format](../../aspose.words.drawing.charts/chartmarker/format/) { get; } | 提供对此标记的填充和线条格式的访问。 |
| [Size](../../aspose.words.drawing.charts/chartmarker/size/) { get; set; } | 获取或设置图表标记大小。 默认值为 7。 |
| [Symbol](../../aspose.words.drawing.charts/chartmarker/symbol/) { get; set; } | 获取或设置图表标记符号。 |

### 例子

显示如何使用折线图上的数据点。

```csharp
[Test]
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

    // 通过使它们显示为菱形来强调图表的数据点。
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // 平滑表示第一个数据系列的线。
    chart.Series[0].Smooth = true;

    // 如果值为负数，则验证第一个系列的数据点不会反转它们的颜色。
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // 为了更清晰的图表，我们可以单独清除格式。
    chart.Series[1].DataPoints[2].ClearFormat();

    // 我们也可以一次剥离整个系列的数据点。
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// 将多个数据点应用于系列。
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


