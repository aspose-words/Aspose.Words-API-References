---
title: Class ChartDataPoint
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartDataPoint сорт. Позволяет задать форматирование одной точки данных на диаграмме.
type: docs
weight: 650
url: /ru/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Позволяет задать форматирование одной точки данных на диаграмме.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } |  |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Предоставляет доступ к заполнению и форматированию строки этой точки данных. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Индекс точки данных, к которой этот объект применяет форматирование. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } |  |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } |  |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Очищает формат этой точки данных. Для свойств установлены значения по умолчанию, определенные в родительской серии. |

### Примечания

В сериале`ChartDataPoint` объект является членом[`ChartDataPointCollection`](../chartdatapointcollection/) . [`ChartDataPointCollection`](../chartdatapointcollection/) содержит`ChartDataPoint` объект для каждой точки.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


