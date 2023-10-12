---
title: Class ChartTitle
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartTitle klass. Ger tillgång till egenskaperna för diagramtiteln.
type: docs
weight: 820
url: /sv/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Ger tillgång till egenskaperna för diagramtiteln.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartTitle
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Bestämmer om andra diagramelement ska tillåtas att överlappa titel. Som standard är överlagring`falsk` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Bestämmer om titeln ska visas för detta diagram. Standardvärdet är`Sann` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Hämtar eller ställer in texten i diagrammets titel. Om`null` eller tomt värde anges, kommer automatiskt genererad titel att visas. |

### Exempel

Visar hur man infogar ett diagram och ställer in en titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en diagramform med en dokumentbyggare och få dess diagram.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Använd egenskapen "Titel" för att ge vårt diagram en titel, som visas högst upp i mitten av diagramområdet.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Ställ in egenskapen "Show" till "true" för att göra titeln synlig.
title.Show = true;

// Ställ in egenskapen "Overlay" på "true" Ge andra diagramelement mer utrymme genom att tillåta dem att överlappa titeln
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


