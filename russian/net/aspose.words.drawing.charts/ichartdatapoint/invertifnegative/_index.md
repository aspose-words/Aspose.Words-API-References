---
title: IChartDataPoint.InvertIfNegative
second_title: Справочник по API Aspose.Words для .NET
description: IChartDataPoint свойство. Указывает должен ли родительский элемент инвертировать свои цвета если значение отрицательное.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/ichartdatapoint/invertifnegative/
---
## IChartDataPoint.InvertIfNegative property

Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное.

```csharp
public bool InvertIfNegative { get; set; }
```

### Примеры

Показывает, как работать с точками данных на линейной диаграмме.

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

    // Подчеркните точки данных диаграммы, сделав их ромбовидными.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Сглаживаем линию, представляющую первый ряд данных.
    chart.Series[0].Smooth = true;

    // Убедитесь, что точки данных для первого ряда не инвертируют свои цвета, если значение отрицательное.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Чтобы график выглядел чище, мы можем очистить формат по отдельности.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Мы также можем сразу удалить всю серию точек данных.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Применяет ряд точек данных к ряду.
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

### Смотрите также

* interface [IChartDataPoint](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* сборка [Aspose.Words](../../../)


