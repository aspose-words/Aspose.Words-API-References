---
title: Class ChartXValueCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartXValueCollection сорт. Представляет коллекцию значений X для серии диаграмм.
type: docs
weight: 850
url: /ru/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Представляет коллекцию значений X для серии диаграмм.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Получает количество элементов в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Получает или задает значение X по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Возвращает объект перечислителя. |

### Примечания

Все предметы коллекции, кроме **нулевой** должно быть то же самое[`ValueType`](../chartxvalue/valuetype/).

Коллекция позволяет изменять только значения X. Чтобы добавить или вставить новые значения в серию диаграмм или удалить значения, соответствующие методы[`ChartSeries`](../chartseries/) класс можно использовать.

### Примеры

Показывает, как получить данные серии диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Очистить индивидуальный формат всех точек данных.
    // Точки данных и значения данных в столбчатых диаграммах взаимно однозначны.
    series.DataPoints[i].ClearFormat();

    // Получаем значение Y.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Изменяем цвета максимального и минимального значений.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Смотрите также

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


