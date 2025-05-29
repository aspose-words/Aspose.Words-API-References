---
title: ChartLegend.LegendEntries
linktitle: LegendEntries
articleTitle: LegendEntries
second_title: Aspose.Words для .NET
description: Изучите свойство ChartLegend LegendEntries, чтобы получить доступ к полной коллекции записей легенд для всех рядов и линий тренда на вашей диаграмме.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

Возвращает коллекцию записей легенды для всех серий и линий тренда родительской диаграммы.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

## Примеры

Показывает, как работать с записью легенды для серии диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Смотрите также

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
