---
title: IChartDataPoint Interface
linktitle: IChartDataPoint
articleTitle: IChartDataPoint
second_title: Aspose.Words для .NET
description: Исследуйте интерфейс Aspose.Words.Drawing.Charts.IChartDataPoint для получения подробных свойств точек данных диаграммы. Улучшите визуализацию данных без усилий!
type: docs
weight: 1220
url: /ru/net/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface

Содержит свойства одной точки данных на диаграмме.

```csharp
public interface IChartDataPoint
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/ichartdatapoint/bubble3d/) { get; set; } | Указывает, следует ли применять к пузырькам на пузырьковой диаграмме 3-D-эффект. |
| [Explosion](../../aspose.words.drawing.charts/ichartdatapoint/explosion/) { get; set; } | Указывает величину, на которую точка данных должна быть перемещена из центра круговой диаграммы. Может быть отрицательным; отрицательное значение означает, что свойство не задано и не должно применяться разбиение. Применяется только к круговым диаграммам. |
| [InvertIfNegative](../../aspose.words.drawing.charts/ichartdatapoint/invertifnegative/) { get; set; } | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [Marker](../../aspose.words.drawing.charts/ichartdatapoint/marker/) { get; } | Указывает маркер данных. Маркер создается автоматически при запросе. |

## Примеры

Показывает, как работать с точками данных на линейном графике.

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

    // Выделите точки данных на диаграмме, придав им форму ромбов.
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

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Для более четкого вида графика мы можем очистить формат по отдельности.
    dataPoint.ClearFormat();

    // Мы также можем удалить целую серию точек данных за один раз.
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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
