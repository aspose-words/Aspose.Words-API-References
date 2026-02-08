---
title: ChartTitle.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: ChartTitle Rotation property. Gets or sets the rotation of the chart title in degrees.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/charttitle/rotation/
---
## ChartTitle.Rotation property

Gets or sets the rotation of the chart title in degrees.

```csharp
public int Rotation { get; set; }
```

## Remarks

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.

## Examples

Shows how to set orientation and rotation of chart and axis titles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

chart.Title.Text = "Sample Chart";
chart.Title.Orientation = ShapeTextOrientation.Horizontal;
chart.Title.Rotation = 90;

// Before setting title properties, make sure that this title will be displayed.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Text = "X Axis";
chart.AxisX.Title.Orientation = ShapeTextOrientation.Horizontal;
chart.AxisX.Title.Rotation = -90;

doc.Save(ArtifactsDir + "Charts.TitleOrientation.docx");
```

### See Also

* class [ChartTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
