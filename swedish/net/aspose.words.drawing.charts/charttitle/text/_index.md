---
title: ChartTitle.Text
second_title: Aspose.Words för .NET API Referens
description: ChartTitle fast egendom. Hämtar eller ställer in texten i diagrammets titel. Omnull eller tomt värde anges kommer automatiskt genererad titel att visas.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Hämtar eller ställer in texten i diagrammets titel. Om`null` eller tomt värde anges, kommer automatiskt genererad titel att visas.

```csharp
public string Text { get; set; }
```

### Anmärkningar

Använda sig av[`Show`](../show/) alternativet om du behöver dölja titeln.

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

* class [ChartTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../charttitle/)
* hopsättning [Aspose.Words](../../../)


