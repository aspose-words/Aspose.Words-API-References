---
title: Enum MarkerSymbol
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.MarkerSymbol 枚举. 指定标记符号样式
type: docs
weight: 920
url: /zh/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

指定标记符号样式。

```csharp
public enum MarkerSymbol
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Default | `0` | 指定应在每个数据点绘制默认标记符号。 |
| Circle | `1` | 指定应在每个数据点处绘制一个圆。 |
| Dash | `2` | 指定应在每个数据点处绘制破折号。 |
| Diamond | `3` | 指定应在每个数据点绘制菱形。 |
| Dot | `4` | 指定应在每个数据点绘制一个点。 |
| None | `5` | 指定在每个数据点处不应绘制任何内容。 |
| Picture | `6` | 指定应在每个数据点绘制图片。 |
| Plus | `7` | 指定应在每个数据点处绘制加号。 |
| Square | `8` | 指定应在每个数据点绘制一个正方形。 |
| Star | `9` | 指定应在每个数据点绘制一颗星。 |
| Triangle | `10` | 指定应在每个数据点绘制一个三角形。 |
| X | `11` | 指定应在每个数据点处绘制 X。 |

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


