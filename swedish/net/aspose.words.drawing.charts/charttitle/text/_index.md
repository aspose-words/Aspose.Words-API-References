---
title: ChartTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Anpassa din diagramtitel enkelt! Ställ in eller hämta egenskapen ChartTitle Text för en personlig touch. Generera titlar automatiskt vid behov.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Hämtar eller ställer in texten i diagrammets titel. Om`null` eller om ett tomt värde anges visas den automatiskt genererade titeln.

```csharp
public string Text { get; set; }
```

## Anmärkningar

Använda[`Show`](../show/) alternativ om du behöver dölja titeln.

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
