---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartDataTable för att enkelt anpassa diagramdatatabeller och förbättra din datavisualisering med kraftfulla funktioner.
type: docs
weight: 990
url: /sv/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Gör det möjligt att ange egenskaper för en diagramdatatabell.

```csharp
public class ChartDataTable
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Ger åtkomst till teckensnittsformatering av datatabellen. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Ger åtkomst till att fylla textbakgrund och formatera kantlinjer för datatabellen. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Hämtar eller ställer in en flagga som anger om en horisontell kantlinje för datatabellen visas. Standardvärdet är`sann` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Hämtar eller ställer in en flagga som anger om förklaringsnycklar visas i datatabellen. Standardvärdet är`sann` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Hämtar eller ställer in en flagga som anger om en konturkant, det vill säga en kant runt serie- och kategorinamn, visas. Standardvärdet är`sann` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Hämtar eller ställer in en flagga som anger om en vertikal kantlinje för datatabellen visas. Standardvärdet är`sann` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Hämtar eller ställer in en flagga som anger om datatabellen ska visas för diagrammet. Standardvärdet är`falsk` . |

## Exempel

Visar hur man visar datatabeller med diagramseriedata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
