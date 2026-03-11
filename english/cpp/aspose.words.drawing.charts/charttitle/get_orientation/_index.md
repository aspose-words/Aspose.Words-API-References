---
title: Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation method
linktitle: get_Orientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation method. Gets or sets the orientation of the chart title text in C++.'
type: docs
weight: 1875
url: /cpp/aspose.words.drawing.charts/charttitle/get_orientation/
---
## ChartTitle::get_Orientation method


Gets or sets the orientation of the chart title text.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation()
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

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
