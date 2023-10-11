---
title: ChartLegendEntry.Font
second_title: Справочник по API Aspose.Words для .NET
description: ChartLegendEntry свойство. Предоставляет доступ к форматированию шрифта этой записи легенды.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Предоставляет доступ к форматированию шрифта этой записи легенды.

```csharp
public Font Font { get; }
```

### Примеры

Показывает, как работать с записью легенды для серий диаграмм.

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

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Смотрите также

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chartlegendentry/)
* сборка [Aspose.Words](../../../)


