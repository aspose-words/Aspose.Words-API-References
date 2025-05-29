---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartTitle för att enkelt hantera och anpassa dina diagramtitlar för förbättrad datavisualisering.
type: docs
weight: 1140
url: /sv/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Ger åtkomst till egenskaperna för diagramtiteln.

För att lära dig mer, besök[Arbeta med -diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartTitle
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Ger åtkomst till teckensnittsformateringen för diagramrubriken. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering av diagramtiteln. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Avgör om andra diagramelement ska tillåtas överlappa titeln. Som standard är överlagring`falsk` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Avgör om titeln ska visas för detta diagram. Standardvärdet är`sann` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Hämtar eller ställer in texten i diagrammets titel. Om`null` eller om ett tomt värde anges visas den automatiskt genererade titeln. |

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
