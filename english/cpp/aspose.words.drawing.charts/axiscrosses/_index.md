---
title: Aspose::Words::Drawing::Charts::AxisCrosses enum
linktitle: AxisCrosses
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisCrosses enum. Specifies the possible crossing points for an axis in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enum


Specifies the possible crossing points for an axis.

```cpp
enum class AxisCrosses
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Automatic | 0 | The category axis crosses at the zero point of the value axis (if possible), or at the minimum value if the minimum is greater than zero, or at the maximum if the maximum is less than zero. |
| Maximum | 1 | A perpendicular axis crosses at the maximum value of the axis. |
| Minimum | 2 | A perpendicular axis crosses at the minimum value of the axis. |
| Custom | 3 | A perpendicular axis crosses at the specified value of the axis. |


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
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

SharedPtr<ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(AxisCategoryType::Automatic);
yAxis->set_Crosses(AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(AxisTickMark::Inside);
yAxis->set_MinorTickMark(AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(AxisTickLabelPosition::NextToAxis);

// Column charts do not have a Z-axis.
ASSERT_TRUE(chart->get_AxisZ() == nullptr);

doc->Save(ArtifactsDir + u"Charts.AxisProperties.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
