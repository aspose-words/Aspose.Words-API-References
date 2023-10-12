---
title: Class ChartDataPointCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartDataPointCollection сорт. Представляет коллекциюChartDataPoint .
type: docs
weight: 700
url: /ru/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Представляет коллекцию[`ChartDataPoint`](../chartdatapoint/) .

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

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
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(int, int) |  |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Возвращает объект перечислителя. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(int) |  |

### Примеры

Показывает, как работать с точками данных на линейной диаграмме.

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

    // Выделите точки данных диаграммы, придав им вид ромба.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Сглаживаем линию, представляющую первый ряд данных.
    chart.Series[0].Smooth = true;

    // Убедитесь, что точки данных для первой серии не инвертируют свои цвета, если значение отрицательное.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Чтобы график выглядел чище, мы можем очистить формат индивидуально.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Мы также можем удалить сразу всю серию точек данных.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Применяет к ряду несколько точек данных.
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


