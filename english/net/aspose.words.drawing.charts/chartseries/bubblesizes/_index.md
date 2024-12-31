---
title: ChartSeries.BubbleSizes
linktitle: BubbleSizes
articleTitle: BubbleSizes
second_title: Aspose.Words for .NET
description: ChartSeries BubbleSizes property. Gets a collection of bubble sizes for this chart series in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/chartseries/bubblesizes/
---
## ChartSeries.BubbleSizes property

Gets a collection of bubble sizes for this chart series.

```csharp
public BubbleSizeCollection BubbleSizes { get; }
```

## Examples

Shows how to work with the format code of the chart data.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a Bubble chart.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Delete default generated series.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Show data labels.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Set data format codes.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### See Also

* class [BubbleSizeCollection](../../bubblesizecollection/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
