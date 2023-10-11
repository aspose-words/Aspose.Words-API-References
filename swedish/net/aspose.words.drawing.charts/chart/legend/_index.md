---
title: Chart.Legend
second_title: Aspose.Words för .NET API Referens
description: Chart fast egendom. Ger tillgång till diagramförklaringsegenskaperna.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Ger tillgång till diagramförklaringsegenskaperna.

```csharp
public ChartLegend Legend { get; }
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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chart/)
* hopsättning [Aspose.Words](../../../)


