---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartNumberFormat för avancerad talformatering i diagram. Förbättra ditt dokuments visuella attraktionskraft!
type: docs
weight: 1060
url: /sv/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Representerar numerisk formatering av det överordnade elementet.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartNumberFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Hämtar eller ställer in formatkoden som tillämpas på en dataetikett. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Anger om formatkoden är länkad till en källcell. Standardvärdet är sant. |

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
