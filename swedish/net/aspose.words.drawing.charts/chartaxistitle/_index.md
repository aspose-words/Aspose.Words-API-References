---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.ChartAxisTitle för att enkelt hantera axeltitelegenskaper och förbättra dokumentets visuella effekt.
type: docs
weight: 910
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Ger åtkomst till axeltitelegenskaperna.

För att lära dig mer, besök[Arbeta med -diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartAxisTitle
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Ger åtkomst till teckensnittsformateringen för axeltiteln. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering av axelrubriken. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Avgör om andra diagramelement ska tillåtas överlappa titeln. Standardvärdet är`falsk` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Avgör om titeln ska visas för axeln. Standardvärdet är`falsk` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Hämtar eller ställer in texten i axelrubriken. Om`null` eller om ett tomt värde anges visas den automatiskt genererade titeln. |

## Exempel

Visar hur man ställer in diagramaxelns titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Radera standardgenererad serie.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
