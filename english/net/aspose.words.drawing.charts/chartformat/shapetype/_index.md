---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words for .NET
description: ChartFormat ShapeType property. Gets or sets the shape type of the parent chart element in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Gets or sets the shape type of the parent chart element.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## Remarks

Currently, the property can only be used for data labels.

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

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
