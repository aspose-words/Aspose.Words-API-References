---
title: Class ChartSeriesCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection сорт. Представляет наборChartSeries .
type: docs
weight: 740
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Представляет набор[`ChartSeries`](../chartseries/) .

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Возвращает количество[`ChartSeries`](../chartseries/) в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Возвращает[`ChartSeries`](../chartseries/) по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(string, DateTime[], double[]) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов к любому типу площадных, радарных и фондовых диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(string, double[], double[]) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии к любому типу точечных диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(string, string[], double[]) | Добавляет новый[`ChartSeries`](../chartseries/)в эту коллекцию. Используйте этот метод для добавления рядов к любым типам гистограмм, столбцов, линейных и поверхностных диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(string, double[], double[], double[]) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в пузырьковые диаграммы любого типа. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Удаляет все[`ChartSeries`](../chartseries/) из этой коллекции. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Возвращает объект перечислителя. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(int) | Удаляет[`ChartSeries`](../chartseries/) по указанному индексу. |

### Примеры

Показывает, как добавлять и удалять ряды данных на диаграмме.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте столбчатую диаграмму, которая по умолчанию будет содержать три ряда демонстрационных данных.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Каждая серия имеет четыре десятичных значения: по одному для каждой из четырех категорий.
// Четыре кластера из трех столбцов будут представлять эти данные.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Вывести название каждой серии на диаграмме.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Это названия категорий на графике.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Мы можем добавить серию с новыми значениями для существующих категорий.
// Эта диаграмма теперь будет содержать четыре кластера по четыре столбца.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });

// Серия диаграмм также может быть удалена по индексу, как здесь.
// Это удалит одну из трех демонстрационных серий, поставляемых с диаграммой.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));

// С помощью этого метода мы также можем очистить все данные графика сразу.
// При создании нового графика это способ стереть все демонстрационные данные
// прежде чем мы сможем начать работу с пустой диаграммой.
chartData.Clear();
```

### Смотрите также

* class [ChartSeries](../chartseries/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


