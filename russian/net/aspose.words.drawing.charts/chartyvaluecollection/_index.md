---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartYValueCollection — ваше идеальное решение для эффективного управления значениями Y в рядах диаграмм.
type: docs
weight: 1200
url: /ru/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

Представляет коллекцию значений Y для серии диаграмм.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Получает количество элементов в этой коллекции. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | Возвращает или задает код формата, применяемый к значениям Y. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Получает или задает значение Y по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Возвращает объект перечислителя. |

## Примечания

Все предметы коллекции, кроме**нулевой** должны иметь то же самое[`ValueType`](../chartyvalue/valuetype/).

Коллекция позволяет изменять только значения Y. Чтобы добавить или вставить новые значения в ряд диаграммы или удалить значения, соответствующие методы[`ChartSeries`](../chartseries/) класс может быть использован.

## Примеры

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
    // Точки данных и значения данных в столбчатых диаграммах соответствуют друг другу.
    series.DataPoints[i].ClearFormat();

    // Получить значение Y.
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

// Изменить цвета максимальных и минимальных значений.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Смотрите также

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
