---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection сорт. Представляет коллекциюChartSeries  на С#.
type: docs
weight: 790
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Представляет коллекцию[`ChartSeries`](../chartseries/) .

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

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
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, DateTime[], double[]*) | Добавляет новые[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий к любым типам площадных, радарных и биржевых диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, double[], double[]*) | Добавляет новые[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в точечные диаграммы любого типа. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, string[], double[]*) | Добавляет новые[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в линейчатые, столбчатые, линейные и поверхностные диаграммы любого типа. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[], double[], double[]*) | Добавляет новые[`ChartSeries`](../chartseries/)в эту коллекцию. Используйте этот метод для добавления рядов в пузырьковые диаграммы любого типа. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Удаляет все[`ChartSeries`](../chartseries/) из этой коллекции. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Возвращает объект перечислителя. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Удаляет[`ChartSeries`](../chartseries/) по указанному индексу. |

## Примеры

Показывает, как добавлять и удалять данные рядов на диаграмме.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем столбчатую диаграмму, которая по умолчанию будет содержать три серии демонстрационных данных.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Каждая серия имеет четыре десятичных значения: по одному для каждой из четырех категорий.
// Эти данные будут представлять четыре кластера по три столбца.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Печатаем имя каждой серии на диаграмме.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Это названия категорий на диаграмме.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Мы можем добавить серию с новыми значениями для существующих категорий.
// Эта диаграмма теперь будет содержать четыре кластера по четыре столбца.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Серию диаграмм также можно удалить по индексу, вот так.
// Это приведет к удалению одной из трех демонстрационных серий, поставляемых с диаграммой.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// С помощью этого метода мы также можем очистить все данные диаграммы одновременно.
// При создании нового графика таким образом можно стереть все демонстрационные данные
// прежде чем мы сможем начать работать с пустым графиком.
chartData.Clear();
```

### Смотрите также

* class [ChartSeries](../chartseries/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
