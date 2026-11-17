---
title: Aspose::Words::Drawing::Charts::ChartTitle::set_Rotation method
linktitle: set_Rotation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartTitle::set_Rotation method. Sets the rotation of the chart title in degrees in C++.'
type: docs
weight: 7500
url: /cpp/aspose.words.drawing.charts/charttitle/set_rotation/
---
## ChartTitle::set_Rotation method


Sets the rotation of the chart title in degrees.

```cpp
void Aspose::Words::Drawing::Charts::ChartTitle::set_Rotation(int32_t value)
```

## Remarks

 The range of acceptable values is from -180 to 180 inclusive. The default value is 0. 
## Examples


Shows how to set orientation and rotation of chart and axis titles.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(ChartType::Column, static_cast<double>(400), static_cast<double>(300));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Before setting title properties, make sure that this title will be displayed.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```
## See Also

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
