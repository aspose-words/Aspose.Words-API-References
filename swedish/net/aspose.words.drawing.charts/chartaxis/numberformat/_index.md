---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartAxis NumberFormat för att enkelt anpassa diagrammets talformat med ChartNumberFormat-objektet för förbättrad datavisualisering.
type: docs
weight: 200
url: /sv/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Returnerar en[`ChartNumberFormat`](../../chartnumberformat/) objekt som tillåter definition av talformat för axeln.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## Exempel

Visar hur man ställer in formatering för diagramvärden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie i diagrammet med kategorier för X-axeln,
 // och stora respektive numeriska värden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Ställ in talformatet för Y-axelns tick-etiketter så att siffror inte grupperas med kommatecken.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Denna flagga kan åsidosätta ovanstående värde och hämta talformatet från källcellen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Se även

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
