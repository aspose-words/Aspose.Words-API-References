---
title: "ChartAxis"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 600
url: /net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Represents the axis options of the chart.

```csharp
public class ChartAxis
```

## Public Members

| Name | Description |
| --- | --- |
| [AxisBetweenCategories](axisbetweencategories) { get; set; } | Gets or sets a flag indicating whether the value axis crosses the category axis between categories. |
| [BaseTimeUnit](basetimeunit) { get; set; } | Returns or sets the smallest time unit that is represented on the time category axis. |
| [CategoryType](categorytype) { get; set; } | Gets or sets type of the category axis. |
| [Crosses](crosses) { get; set; } | Specifies how this axis crosses the perpendicular axis. |
| [CrossesAt](crossesat) { get; set; } | Specifies where on the perpendicular axis the axis crosses. |
| [DisplayUnit](displayunit) { get; } | Specifies the scaling value of the display units for the value axis. |
| [Document](document) { get; } | Returns the Document the title holder belongs. |
| [Hidden](hidden) { get; set; } | Gets or sets a flag indicating whether this axis is hidden or not. |
| [MajorTickMark](majortickmark) { get; set; } | Returns or sets the major tick marks. |
| [MajorUnit](majorunit) { get; set; } | Returns or sets the distance between major tick marks. |
| [MajorUnitIsAuto](majorunitisauto) { get; set; } | Gets or sets a flag indicating whether default distance between major tick marks shall be used. |
| [MajorUnitScale](majorunitscale) { get; set; } | Returns or sets the scale value for major tick marks on the time category axis. |
| [MinorTickMark](minortickmark) { get; set; } | Returns or sets the minor tick marks for the axis. |
| [MinorUnit](minorunit) { get; set; } | Returns or sets the distance between minor tick marks. |
| [MinorUnitIsAuto](minorunitisauto) { get; set; } | Gets or sets a flag indicating whether default distance between minor tick marks shall be used. |
| [MinorUnitScale](minorunitscale) { get; set; } | Returns or sets the scale value for minor tick marks on the time category axis. |
| [NumberFormat](numberformat) { get; } | Returns a [`ChartNumberFormat`](../chartnumberformat) object that allows defining number formats for the axis. |
| [ReverseOrder](reverseorder) { get; set; } | Returns or sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. |
| [Scaling](scaling) { get; } | Provides access to the scaling options of the axis. |
| [TickLabelAlignment](ticklabelalignment) { get; set; } | Gets or sets text alignment of axis tick labels. |
| [TickLabelOffset](ticklabeloffset) { get; set; } | Gets or sets the distance of labels from the axis. |
| [TickLabelPosition](ticklabelposition) { get; set; } | Returns or sets the position of the tick labels on the axis. |
| [TickLabelSpacing](ticklabelspacing) { get; set; } | Gets or sets the interval, at which tick labels are drawn. |
| [TickLabelSpacingIsAuto](ticklabelspacingisauto) { get; set; } | Gets or sets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [TickMarkSpacing](tickmarkspacing) { get; set; } | Gets or sets the interval, at which tick marks are drawn. |
| [Type](type) { get; } | Returns type of the axis. |

### Examples

Shows how to insert a chart and modify the appearance of its axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Chart axes have various options that can change their appearance,
// such as their direction, major/minor unit ticks, and tick marks.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Column charts do not have a Z-axis.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
