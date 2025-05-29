---
title: ChartLegend.LegendEntries
linktitle: LegendEntries
articleTitle: LegendEntries
second_title: Aspose.Words för .NET
description: Utforska egenskapen ChartLegend LegendEntries för att få tillgång till en omfattande samling av förklaringsposter för alla serier och trendlinjer i ditt diagram.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

Returnerar en samling förklaringsposter för alla serier och trendlinjer i det överordnade diagrammet.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

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

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
