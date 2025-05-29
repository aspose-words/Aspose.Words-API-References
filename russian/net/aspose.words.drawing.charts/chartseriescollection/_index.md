---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartSeriesCollection — решение для простого управления и настройки серий диаграмм.
type: docs
weight: 1080
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Представляет собой коллекцию[`ChartSeries`](../chartseries/) .

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

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
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[]*) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в гистограммы. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, ChartMultilevelValue[], double[]*) | Добавляет новый[`ChartSeries`](../chartseries/)в эту коллекцию. Используйте этот метод для добавления рядов, имеющих многоуровневые категории данных. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_4)(*string, DateTime[], double[]*) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в любые типы площадных, радиальных и биржевых диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, double[], double[]*) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в любые типы диаграмм рассеяния. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_5)(*string, string[], double[]*) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в любые типы линейчатых, столбчатых, линейных и поверхностных диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, double[], double[], double[]*) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в любые типы пузырьковых диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_6)(*string, string[], double[], bool[]*) | Добавляет новый[`ChartSeries`](../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в каскадные диаграммы. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Удаляет все[`ChartSeries`](../chartseries/) из этой коллекции. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Возвращает объект перечислителя. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Удаляет[`ChartSeries`](../chartseries/) по указанному индексу. |

## Примеры

Показывает, как добавлять и удалять ряды данных на диаграмме.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте столбчатую диаграмму, которая по умолчанию будет содержать три серии демонстрационных данных.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Каждая серия имеет четыре десятичных значения: по одному для каждой из четырех категорий.
// Четыре кластера по три столбца будут представлять эти данные.
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

// Это названия категорий в таблице.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Мы можем добавить серию с новыми значениями для существующих категорий.
// Теперь эта диаграмма будет содержать четыре кластера по четыре столбца.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Серию диаграмм также можно удалить по индексу, вот так.
// Это приведет к удалению одной из трех демонстрационных серий, поставляемых с диаграммой.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// С помощью этого метода мы также можем очистить все данные диаграммы одновременно.
// При создании нового графика это способ стереть все демонстрационные данные
// прежде чем мы начнем работать с пустой диаграммой.
chartData.Clear();
```

### Смотрите также

* class [ChartSeries](../chartseries/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
