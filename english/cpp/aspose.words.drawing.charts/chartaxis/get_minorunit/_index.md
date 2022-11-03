---
title: get_MinorUnit
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the distance between minor tick marks.
type: docs
weight: 170
url: /cpp/aspose.words.drawing.charts/chartaxis/get_minorunit/
---
## ChartAxis.get_MinorUnit method


Returns or sets the distance between minor tick marks.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit()
```


Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [MinorUnitIsAuto](../get_minorunitisauto/) property to **false**.

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
