---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartDataPoint, который позволяет легко форматировать отдельные точки данных диаграммы, повышая точность визуализации данных.
type: docs
weight: 970
url: /ru/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Позволяет указать форматирование отдельной точки данных на диаграмме.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Указывает, следует ли применять к пузырькам на пузырьковой диаграмме 3-D-эффект. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Указывает величину, на которую точка данных должна быть перемещена из центра круговой диаграммы. Может быть отрицательным; отрицательное значение означает, что свойство не задано и не должно применяться разбиение. Применяется только к круговым диаграммам. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Предоставляет доступ к заполнению и форматированию линий этой точки данных. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Индекс точки данных, к которой этот объект применяет форматирование. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Указывает маркер данных диаграммы. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Очищает формат этой точки данных. Свойства устанавливаются на значения по умолчанию, определенные в родительской серии. |

## Примечания

В серии,`ChartDataPoint` объект является членом[`ChartDataPointCollection`](../chartdatapointcollection/) . [`ChartDataPointCollection`](../chartdatapointcollection/) содержит`ChartDataPoint` объект для каждой точки.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
