---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ChartFormat för avancerad stilisering av diagramelement. Förbättra dina dokument med professionella, anpassningsbara diagramdesigner.
type: docs
weight: 1000
url: /sv/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Representerar formateringen av ett diagramelement.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Hämtar fyllningsformatering för det överordnade diagramelementet. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Hämtar en flagga som anger om något format är definierat. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Hämtar eller anger formtypen för det överordnade diagramelementet. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Hämtar linjeformatering för det överordnade diagramelementet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Återställer fyllningen av diagramelementet till standardvärdet. |

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
