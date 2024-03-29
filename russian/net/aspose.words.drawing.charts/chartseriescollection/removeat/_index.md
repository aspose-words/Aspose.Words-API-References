---
title: ChartSeriesCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words для .NET
description: ChartSeriesCollection RemoveAt метод. УдаляетChartSeries по указанному индексу на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/removeat/
---
## ChartSeriesCollection.RemoveAt method

Удаляет[`ChartSeries`](../../chartseries/) по указанному индексу.

```csharp
public void RemoveAt(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс, отсчитываемый от нуля[`ChartSeries`](../../chartseries/) удалять. |

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

* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
