---
title: ChartLegend.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Diagramförklaringsformat för enkel anpassning av förklaringsfyllning och linjestilar, vilket förbättrar din datavisualiseringsupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartlegend/format/
---
## ChartLegend.Format property

Ger åtkomst till fyllnings- och linjeformatering av förklaringen.

```csharp
public ChartFormat Format { get; }
```

## Exempel

Visar hur man använder diagramformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Radera serier som genereras som standard.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formatera diagrambakgrund.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Dölj axeltackningsetiketter.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formatera diagramtitel.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatera axeltitel.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatförklaring.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Se även

* class [ChartFormat](../../chartformat/)
* class [ChartLegend](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
