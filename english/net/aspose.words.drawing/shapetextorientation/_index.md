---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ShapeTextOrientation enum. Specifies orientation of text in shapes in C#.
type: docs
weight: 1540
url: /net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Specifies orientation of text in shapes.

```csharp
public enum ShapeTextOrientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | `0` | Text is arranged horizontally (lr-tb). |
| Downward | `1` | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| Upward | `2` | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| VerticalFarEast | `3` | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally (tb-lr-v). |
| WordArtVertical | `5` | Text is vertical, with one letter on top of the other. |
| WordArtVerticalRightToLeft | `6` | Text is vertical, with one letter on top of the other, then right to left horizontally. |

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
