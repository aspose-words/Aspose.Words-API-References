---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.Drawing.Charts.MarkerSymbol для настраиваемых стилей маркеров, которые улучшают визуальные эффекты диаграмм и представление данных.
type: docs
weight: 1240
url: /ru/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Задает стиль символа маркера.

```csharp
public enum MarkerSymbol
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Указывает, что символ маркера по умолчанию должен быть нарисован в каждой точке данных. |
| Circle | `1` | Указывает, что в каждой точке данных должен быть нарисован круг. |
| Dash | `2` | Указывает, что в каждой точке данных должна быть нарисована черточка. |
| Diamond | `3` | Указывает, что в каждой точке данных должен быть нарисован ромб. |
| Dot | `4` | Указывает, что точка должна быть нарисована в каждой точке данных. |
| None | `5` | Указывает, что в каждой точке данных ничего не должно отображаться. |
| Picture | `6` | Указывает, что изображение должно быть нарисовано в каждой точке данных. |
| Plus | `7` | Указывает, что в каждой точке данных должен быть изображен знак плюса. |
| Square | `8` | Указывает, что в каждой точке данных должен быть нарисован квадрат. |
| Star | `9` | Указывает, что в каждой точке данных должна быть нарисована звездочка. |
| Triangle | `10` | Указывает, что в каждой точке данных должен быть нарисован треугольник. |
| X | `11` | Указывает, что в каждой точке данных должен быть нарисован символ X. |

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
