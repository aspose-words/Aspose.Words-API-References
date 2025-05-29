---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartXValue — ваше решение для определения значений X в рядах диаграмм, которое легко улучшает визуализацию данных.
type: docs
weight: 1160
url: /ru/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Представляет значение X для серии диаграмм.

```csharp
public class ChartXValue
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Получает сохраненное значение даты и времени. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Получает сохраненное числовое значение. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Получает сохраненное многоуровневое значение. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Получает сохраненное строковое значение. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Получает сохраненное значение времени. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Возвращает тип значения X, хранящегося в объекте. |

## Методы

| Имя | Описание |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Создает`ChartXValue` примерDateTime тип. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Создает`ChartXValue` примерDouble тип. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Создает`ChartXValue` примерMultilevel тип. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Создает`ChartXValue` примерString тип. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Создает`ChartXValue` примерTime тип. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Возвращает флаг, указывающий, равен ли указанный объект текущему значению X object. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Получает хэш-код для текущего объекта значения X. |

## Примечания

Этот класс содержит ряд статических методов для создания значения X определенного типа. The [`ValueType`](./valuetype/) Свойство позволяет определить тип существующего значения X.

Все ненулевые значения X в серии диаграмм должны быть одинаковыми[`ChartXValueType`](../chartxvaluetype/) тип.

## Примеры

Показывает, как заполнить ряды диаграмм данными.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();

// Заполняем ряд данными.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Очистить значения X и Y второй серии.
series2.Clear();

// Заполняем ряд данными.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
