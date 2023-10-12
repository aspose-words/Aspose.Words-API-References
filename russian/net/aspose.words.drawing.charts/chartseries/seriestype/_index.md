---
title: ChartSeries.SeriesType
second_title: Справочник по API Aspose.Words для .NET
description: ChartSeries свойство. Получает тип этой серии диаграмм.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Получает тип этой серии диаграмм.

```csharp
public ChartSeriesType SeriesType { get; }
```

### Примеры

Показывает, как

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Удалить все серии типа Столбец.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### Смотрите также

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chartseries/)
* сборка [Aspose.Words](../../../)


