---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ChartNumberFormat IsLinkedToSource förbättrar din datavisualisering genom att länka formatkoder till källceller. Läs mer nu!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Anger om formatkoden är länkad till en källcell. Standardvärdet är sant.

```csharp
public bool IsLinkedToSource { get; set; }
```

## Anmärkningar

NumberFormat återställs till generellt om formatkod länkas till källkoden.

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

* class [ChartNumberFormat](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
