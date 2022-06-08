---
title: ChartAxis
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 610
url: /net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Represents the axis options of the chart.

```csharp
public class ChartAxis
```

## Properties

| Name | Description |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories) { get; set; } | Gets or sets a flag indicating whether the value axis crosses the category axis between categories. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit) { get; set; } | Returns or sets the smallest time unit that is represented on the time category axis. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype) { get; set; } | Gets or sets type of the category axis. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses) { get; set; } | Specifies how this axis crosses the perpendicular axis. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat) { get; set; } | Specifies where on the perpendicular axis the axis crosses. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit) { get; } | Specifies the scaling value of the display units for the value axis. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document) { get; } | Returns the Document the title holder belongs. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden) { get; set; } | Gets or sets a flag indicating whether this axis is hidden or not. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark) { get; set; } | Returns or sets the major tick marks. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit) { get; set; } | Returns or sets the distance between major tick marks. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto) { get; set; } | Gets or sets a flag indicating whether default distance between major tick marks shall be used. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale) { get; set; } | Returns or sets the scale value for major tick marks on the time category axis. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark) { get; set; } | Returns or sets the minor tick marks for the axis. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit) { get; set; } | Returns or sets the distance between minor tick marks. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto) { get; set; } | Gets or sets a flag indicating whether default distance between minor tick marks shall be used. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale) { get; set; } | Returns or sets the scale value for minor tick marks on the time category axis. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat) { get; } | Returns a [`ChartNumberFormat`](../chartnumberformat) object that allows defining number formats for the axis. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder) { get; set; } | Returns or sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling) { get; } | Provides access to the scaling options of the axis. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment) { get; set; } | Gets or sets text alignment of axis tick labels. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset) { get; set; } | Gets or sets the distance of labels from the axis. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition) { get; set; } | Returns or sets the position of the tick labels on the axis. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing) { get; set; } | Gets or sets the interval, at which tick labels are drawn. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto) { get; set; } | Gets or sets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing) { get; set; } | Gets or sets the interval, at which tick marks are drawn. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type) { get; } | Returns type of the axis. |

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
