---
title: Enum MarkerSymbol
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.MarkerSymbol перечисление. Определяет стиль символа маркера.
type: docs
weight: 920
url: /ru/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Определяет стиль символа маркера.

```csharp
public enum MarkerSymbol
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Указывает, что символ маркера по умолчанию должен отображаться в каждой точке данных. |
| Circle | `1` | Указывает, что в каждой точке данных должен быть нарисован круг. |
| Dash | `2` | Указывает, что в каждой точке данных должно быть нарисовано тире. |
| Diamond | `3` | Указывает, что в каждой точке данных должен быть нарисован ромб. |
| Dot | `4` | Указывает, что в каждой точке данных должна быть нарисована точка. |
| None | `5` | Указывает, что в каждой точке данных ничего не должно отображаться. |
| Picture | `6` | Указывает, что изображение должно быть нарисовано в каждой точке данных. |
| Plus | `7` | Указывает, что в каждой точке данных должен отображаться плюс. |
| Square | `8` | Указывает, что в каждой точке данных должен быть нарисован квадрат. |
| Star | `9` | Указывает, что в каждой точке данных должна быть нарисована звезда. |
| Triangle | `10` | Указывает, что в каждой точке данных должен быть нарисован треугольник. |
| X | `11` | Указывает, что в каждой точке данных должен быть нарисован X. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


