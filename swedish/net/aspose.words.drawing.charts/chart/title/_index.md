---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words för .NET
description: Chart Title fast egendom. Ger tillgång till egenskaperna för diagramtiteln i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Ger tillgång till egenskaperna för diagramtiteln.

```csharp
public ChartTitle Title { get; }
```

## Exempel

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
