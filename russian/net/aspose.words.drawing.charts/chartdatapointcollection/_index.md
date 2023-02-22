---
title: Class ChartDataPointCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartDataPointCollection сорт. Представляет наборChartDataPoint .
type: docs
weight: 660
url: /ru/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Представляет набор[`ChartDataPoint`](../chartdatapoint/) .

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | Возвращает количество[`ChartDataPoint`](../chartdatapoint/) в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Возвращает[`ChartDataPoint`](../chartdatapoint/) для указанного индекса. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Очищает формат всех[`ChartDataPoint`](../chartdatapoint/) в этой коллекции. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Возвращает объект перечислителя. |

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

* class [ChartDataPoint](../chartdatapoint/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


