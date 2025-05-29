---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartLegend Position för att enkelt anpassa diagrammets förklaringsplacering för ökad tydlighet och visuell tilltalning.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Anger förklaringens position i ett diagram.

```csharp
public LegendPosition Position { get; set; }
```

## Anmärkningar

Standardvärdet ärRight för diagram före Word 2016 och Top för Word 2016-diagram.

## Exempel

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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
