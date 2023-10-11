---
title: ChartSeries.Format
second_title: Aspose.Words för .NET API Referens
description: ChartSeries fast egendom. Ger tillgång till fyllnings och radformatering av serien.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Ger tillgång till fyllnings- och radformatering av serien.

```csharp
public ChartFormat Format { get; }
```

### Exempel

Sågar hur man ställer in seriefärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Ta bort standardgenererade serier.
seriesColl.Clear();

// Skapa kategorinamn array.
string[] categories = new[] { "Category 1", "Category 2" };

// Lägger till ny serie. Värde- och kategorimatriser måste ha samma storlek.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Ställ in seriefärg.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Se även

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartseries/)
* hopsättning [Aspose.Words](../../../)


