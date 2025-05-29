---
title: ChartDataTable.HasLegendKeys
linktitle: HasLegendKeys
articleTitle: HasLegendKeys
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartDataTable HasLegendKeys för att enkelt kontrollera synligheten av förklaringsnycklar i din datatabell. Förbättra tydligheten med anpassningsbara inställningar!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartdatatable/haslegendkeys/
---
## ChartDataTable.HasLegendKeys property

Hämtar eller ställer in en flagga som anger om förklaringsnycklar visas i datatabellen. Standardvärdet är`sann` .

```csharp
public bool HasLegendKeys { get; set; }
```

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

* class [ChartDataTable](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
