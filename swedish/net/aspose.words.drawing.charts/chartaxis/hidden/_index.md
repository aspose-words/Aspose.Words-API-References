---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartAxis Hidden för att enkelt hantera axlarnas synlighet i dina diagram. Förbättra din datapresentation med den här enkla växlingsfunktionen!
type: docs
weight: 110
url: /sv/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Hämtar eller ställer in en flagga som anger om denna axel är dold eller inte.

```csharp
public bool Hidden { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man döljer diagramaxlar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie med kategorier för X-axeln och respektive decimalvärden för Y-axeln.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // Dölj diagramaxlarna för att förenkla diagrammets utseende.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Se även

* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
