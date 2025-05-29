---
title: ChartSeries.YValues
linktitle: YValues
articleTitle: YValues
second_title: Aspose.Words för .NET
description: Upptäck egenskapen YValues i ChartSeries för att få tillgång till en kraftfull samling Y-värden, vilket förbättrar dina datavisualiserings- och analysmöjligheter.
type: docs
weight: 150
url: /sv/net/aspose.words.drawing.charts/chartseries/yvalues/
---
## ChartSeries.YValues property

Hämtar en samling Y-värden för denna diagramserie.

```csharp
public ChartYValueCollection YValues { get; }
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

* class [ChartYValueCollection](../../chartyvaluecollection/)
* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
