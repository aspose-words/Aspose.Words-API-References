---
title: ChartAxisTitle.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: ChartAxisTitle Orientation property. Gets or sets the orientation of the axis title text.
type: docs
weight: 30
url: /net/aspose.words.drawing.charts/chartaxistitle/orientation/
---
## ChartAxisTitle.Orientation property

Gets or sets the orientation of the axis title text.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Remarks

The default value is Horizontal.

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartAxisTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
