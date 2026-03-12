---
title: Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation method
linktitle: get_Rotation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation method. Gets or sets the rotation of the axis title in degrees in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words.drawing.charts/chartaxistitle/get_rotation/
---
## ChartAxisTitle::get_Rotation method


Gets or sets the rotation of the axis title in degrees.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation()
```


## Examples



Shows how to set orientation and rotation of chart and axis titles. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Before setting title properties, make sure that this title will be displayed.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## See Also

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
