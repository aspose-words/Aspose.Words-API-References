---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.Charts.LegendPosition-uppräkningen för att enkelt anpassa din diagramförklarings position för förbättrad datavisualisering.
type: docs
weight: 1230
url: /sv/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Anger möjliga positioner för en diagramförklaring.

```csharp
public enum LegendPosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Ingen förklaring kommer att visas för diagrammet. |
| Bottom | `1` | Anger att förklaringen ska ritas längst ner i diagrammet. |
| Left | `2` | Anger att förklaringen ska ritas till vänster i diagrammet. |
| Right | `3` | Anger att förklaringen ska ritas till höger om diagrammet. |
| Top | `4` | Anger att förklaringen ska ritas högst upp i diagrammet. |
| TopRight | `5` | Anger att förklaringen ska ritas längst upp till höger i diagrammet. |

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
