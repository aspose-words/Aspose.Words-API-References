---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeries SeriesType, чтобы легко определить тип серии диаграммы и улучшить визуализацию данных. Откройте для себя мощные идеи сегодня!
type: docs
weight: 120
url: /ru/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Получает тип этой серии диаграмм.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Примеры

Показывает, как удалить определенную серию диаграмм.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Удалить все серии типа «Столбец».
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
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
