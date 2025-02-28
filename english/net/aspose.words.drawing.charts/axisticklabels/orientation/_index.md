---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: Customize your AxisTickLabels orientation for optimal readability. Easily adjust tick label text direction to enhance your data visualization!
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Gets or sets the orientation of the tick label text.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Remarks

The default value is Horizontal.

Note that some [`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) values do not affect the orientation of tick label text in value axes.

## Examples

Shows how to change orientation and rotation for axis tick labels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a column chart.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Set axis tick label orientation and rotation.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### See Also

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
