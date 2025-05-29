---
title: ChartTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words för .NET
description: Förbättra dina diagram med anpassningsbara titlar. Kontrollera synligheten enkelt – standardinställningen är sant. Förbättra din datapresentation idag!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Avgör om titeln ska visas för detta diagram. Standardvärdet är`sann` .

```csharp
public bool Show { get; set; }
```

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

* class [ChartTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
