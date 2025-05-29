---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words för .NET
description: Lås upp kraftfulla egenskaper för diagramformer med klassen Aspose.Words.Drawing.Charts.Chart. Förbättra dina dokument med dynamisk visuell datarepresentation.
type: docs
weight: 880
url: /sv/net/aspose.words.drawing.charts/chart/
---
## Chart class

Ger åtkomst till diagrammets formegenskaper.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class Chart
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Hämtar en samling av alla axlar i detta diagram. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Ger åtkomst till egenskaper för diagrammets primära X-axel. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Ger åtkomst till egenskaper för diagrammets primära Y-axel. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Ger åtkomst till egenskaper för diagrammets Z-axel. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Ger åtkomst till egenskaper för en datatabell i detta diagram. Datatabellen kan visas med hjälp av[`Show`](../chartdatatable/show/) egendom. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering av diagrammet. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Ger åtkomst till egenskaperna för diagramförklaringen. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Ger åtkomst till seriesamlingen. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Ger åtkomst till en seriegruppsamling av detta diagram. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Hämtar sökvägen och namnet på en xls/xlsx-fil som detta diagram är länkat till. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Hämtar eller ställer in diagrammets stil. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Ger åtkomst till egenskaperna för diagramtiteln. |

## Exempel

Visar hur man infogar ett diagram och anger en titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en diagramform med en dokumentbyggare och hämta dess diagram.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Använd egenskapen "Titel" för att ge vårt diagram en titel, som visas högst upp i mitten av diagramområdet.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // Sätt egenskapen "Visa" till "true" för att göra titeln synlig.
title.Show = true;

// Sätt egenskapen "Overlay" till "true" Ge andra diagramelement mer utrymme genom att låta dem överlappa titeln
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
