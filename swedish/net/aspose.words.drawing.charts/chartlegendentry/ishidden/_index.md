---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartLegendEntry IsHidden och kontrollera diagramförklaringens synlighet utan ansträngning. Förbättra din datapresentation med den här enkla växlingsfunktionen!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Hämtar eller ställer in ett värde som anger om den här posten är dold i diagramförklaringen. Standardvärdet är**falsk** .

```csharp
public bool IsHidden { get; set; }
```

## Anmärkningar

När en diagramförklaringspost är dold påverkar det inte motsvarande diagramserie eller trendlinje att fortfarande visas på diagrammet.

## Exempel

Visar hur man arbetar med en förklaringspost för diagramserier.

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

### Se även

* class [ChartLegendEntry](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
