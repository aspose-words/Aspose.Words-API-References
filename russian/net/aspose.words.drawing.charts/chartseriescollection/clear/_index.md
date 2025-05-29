---
title: ChartSeriesCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: Легко очистите все ChartSeries из вашей коллекции с помощью метода ChartSeriesCollection Clear. Оптимизируйте управление данными сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/clear/
---
## ChartSeriesCollection.Clear method

Удаляет все[`ChartSeries`](../../chartseries/) из этой коллекции.

```csharp
public void Clear()
```

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

* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
