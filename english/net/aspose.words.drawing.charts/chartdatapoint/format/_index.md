---
title: ChartDataPoint.Format
linktitle: Format
second_title: Aspose.Words for .NET API Reference
description: ChartDataPoint Format property. Provides access to fill and line formatting of this data point in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Provides access to fill and line formatting of this data point.

```csharp
public ChartFormat Format { get; }
```

## Examples

Shows how to set individual formatting for categories of a column chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Delete default generated series.
chart.Series.Clear();

// Adding new series.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Set column formatting.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### See Also

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartdatapoint/)
* assembly [Aspose.Words](../../../)
