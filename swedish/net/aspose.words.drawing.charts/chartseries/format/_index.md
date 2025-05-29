---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Diagramserieformat för enkel åtkomst till anpassningsbara fyllnings- och linjestilar, vilket förbättrar din datavisualiseringsupplevelse.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Ger åtkomst till fyllnings- och linjeformatering av serien.

```csharp
public ChartFormat Format { get; }
```

## Exempel

Sår hur man ställer in seriefärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Radera standardgenererad serie.
seriesColl.Clear();

// Skapa en array med kategorinamn.
string[] categories = new[] { "Category 1", "Category 2" };

// Lägger till nya serier. Värde- och kategorimatriser måste ha samma storlek.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Ange seriefärg.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Se även

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
