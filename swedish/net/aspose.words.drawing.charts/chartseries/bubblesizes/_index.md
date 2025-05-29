---
title: ChartSeries.BubbleSizes
linktitle: BubbleSizes
articleTitle: BubbleSizes
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeries BubbleSizes för att få tillgång till anpassningsbara bubbelstorlekar, vilket förbättrar din datavisualisering och diagramupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartseries/bubblesizes/
---
## ChartSeries.BubbleSizes property

Hämtar en samling bubbelstorlekar för den här diagramserien.

```csharp
public BubbleSizeCollection BubbleSizes { get; }
```

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

* class [BubbleSizeCollection](../../bubblesizecollection/)
* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
