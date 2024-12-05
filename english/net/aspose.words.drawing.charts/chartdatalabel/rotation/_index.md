---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: ChartDataLabel Rotation property. Gets or sets the rotation of the label in degrees in C#.
type: docs
weight: 110
url: /net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

Gets or sets the rotation of the label in degrees.

```csharp
public int Rotation { get; set; }
```

## Remarks

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.

If the [`Orientation`](../orientation/) value is Horizontal, the label shape, if it exists, is rotated along with the label text. Otherwise, only the label text is rotated.

## Examples

Shows how to change orientation and rotation for data labels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Show data labels.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Define data label shape.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Set data label orientation and rotation for the entire series.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Change orientation and rotation of the first data label.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### See Also

* class [ChartDataLabel](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
