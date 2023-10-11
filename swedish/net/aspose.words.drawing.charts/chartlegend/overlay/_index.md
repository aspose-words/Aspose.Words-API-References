---
title: ChartLegend.Overlay
second_title: Aspose.Words för .NET API Referens
description: ChartLegend fast egendom. Bestämmer om andra diagramelement ska tillåtas att överlappa förklaringen. Standardvärdet ärfalsk .
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Bestämmer om andra diagramelement ska tillåtas att överlappa förklaringen. Standardvärdet är`falsk` .

```csharp
public bool Overlay { get; set; }
```

### Exempel

Visar hur man redigerar utseendet på ett diagrams förklaring.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Flytta diagrammets förklaring till det övre högra hörnet.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Ge andra diagramelement, som grafen, mer utrymme genom att låta dem överlappa förklaringen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Se även

* class [ChartLegend](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartlegend/)
* hopsättning [Aspose.Words](../../../)


