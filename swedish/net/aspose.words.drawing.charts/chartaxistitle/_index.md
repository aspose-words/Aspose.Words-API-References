---
title: Class ChartAxisTitle
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartAxisTitle klass. Ger tillgång till egenskaperna för axeltiteln.
type: docs
weight: 650
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Ger tillgång till egenskaperna för axeltiteln.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartAxisTitle
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Bestämmer om andra diagramelement ska tillåtas överlappa titeln. Standardvärdet är`falsk` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Bestämmer om titeln ska visas för axeln. Standardvärdet är`falsk` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Hämtar eller ställer in texten i axeltiteln. Om`null` eller tomt värde anges, kommer automatiskt genererad titel att visas. |

### Exempel

Visar hur man ställer in diagramaxelns titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Ta bort standardgenererade serier.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Ställ in axeltitel.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


