---
title: get_TickMarkSpacing
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the interval, at which tick marks are drawn.
type: docs
weight: 313
url: /cpp/aspose.words.drawing.charts/chartaxis/get_tickmarkspacing/
---
## ChartAxis.get_TickMarkSpacing method


Gets or sets the interval, at which tick marks are drawn.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing()
```


The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

Valid range of a value is greater than or equal to 1.

## Examples




Shows how to insert a chart and modify the appearance of its axes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Column, 500, 300);
SharedPtr<Chart> chart = shape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart->get_Series()->Add(u"Aspose Test Series", MakeArray<String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}),
                         MakeArray<double>({640, 320, 280, 120, 150}));

// Chart axes have various options that can change their appearance,
// such as their direction, major/minor unit ticks, and tick marks.
SharedPtr<ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(AxisCategoryType::Category);
xAxis->set_Crosses(AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(AxisTickMark::Inside);
xAxis->set_MinorTickMark(AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->set_TickLabelOffset(50);
xAxis->set_TickLabelPosition(AxisTickLabelPosition::Low);
xAxis->set_TickLabelSpacingIsAuto(false);
xAxis->set_TickMarkSpacing(1);

SharedPtr<ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(AxisCategoryType::Automatic);
yAxis->set_Crosses(AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(AxisTickMark::Inside);
yAxis->set_MinorTickMark(AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->set_TickLabelPosition(AxisTickLabelPosition::NextToAxis);

// Column charts do not have a Z-axis.
ASSERT_TRUE(chart->get_AxisZ() == nullptr);

doc->Save(ArtifactsDir + u"Charts.AxisProperties.docx");
```

