---
title: BubbleSizeCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BubbleSizeCollection FormatCode för att enkelt anpassa bubbelstorlekar. Förbättra din datavisualisering med skräddarsydda formateringsalternativ.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/bubblesizecollection/formatcode/
---
## BubbleSizeCollection.FormatCode property

Hämtar eller ställer in formatkoden som tillämpas på bubbelstorlekarna.

```csharp
public string FormatCode { get; set; }
```

## Anmärkningar

Nummerformatering används för att ändra hur värden visas i diagrammet. Exempel på nummerformat:

Nummer - "#,##0.00"

Valuta - "\"$\"#,##0.00"

Tid - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/åååå"

Procentandel - "0,00%"

Bråk - "# ?/?"

Vetenskaplig - "0.00E+00"

Redovisning - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Anpassad med färg - "[Röd]-#,##0.0"

## Exempel

Visar hur man arbetar med formatkoden för diagramdata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett bubbeldiagram.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Radera standardgenererad serie.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Visa dataetiketter.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Ange dataformatkoder.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Se även

* class [BubbleSizeCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
