---
title: ChartAxis.NumberFormat
second_title: Aspose.Words för .NET API Referens
description: ChartAxis fast egendom. Returnerar enChartNumberFormat objekt som tillåter att definiera talformat för axeln.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Returnerar en[`ChartNumberFormat`](../../chartnumberformat/) objekt som tillåter att definiera talformat för axeln.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Exempel

Visar hur du ställer in formatering för diagramvärden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie till diagrammet med kategorier för X-axeln,
 // och stora respektive numeriska värden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Ställ in nummerformatet för Y-axelns bocketiketter för att inte gruppera siffror med kommatecken.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Den här flaggan kan åsidosätta ovanstående värde och rita talformatet från källcellen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Se även

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartaxis/)
* hopsättning [Aspose.Words](../../../)


