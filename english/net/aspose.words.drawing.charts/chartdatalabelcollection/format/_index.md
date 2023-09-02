---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection Format property. Provides access to fill and line formatting of the data labels in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Provides access to fill and line formatting of the data labels.

```csharp
public ChartFormat Format { get; }
```

## Examples

Shows how to set fill, stroke and callout formatting for chart data labels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Delete default generated series.
chart.Series.Clear();

// Add new series.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Show data labels.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Format data labels as callouts.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Change fill and stroke of an individual data label.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### See Also

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
