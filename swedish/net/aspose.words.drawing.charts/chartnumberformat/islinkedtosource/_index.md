---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words för .NET
description: ChartNumberFormat IsLinkedToSource fast egendom. Anger om formatkoden är länkad till en källcell. Standard är true i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Anger om formatkoden är länkad till en källcell. Standard är true.

```csharp
public bool IsLinkedToSource { get; set; }
```

## Anmärkningar

NumberFormat kommer att återställas till allmänt om formatkoden är länkad till källan.

## Exempel

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

* class [ChartNumberFormat](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
