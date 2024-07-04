---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection Orientation property. Gets or sets the text orientation of the data labels of the entire series in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

Gets or sets the text orientation of the data labels of the entire series.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Remarks

The default value is Horizontal.

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
