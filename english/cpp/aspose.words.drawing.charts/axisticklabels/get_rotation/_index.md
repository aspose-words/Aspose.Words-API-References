---
title: Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation method
linktitle: get_Rotation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation method. Gets or sets the rotation of the tick labels in degrees in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/axisticklabels/get_rotation/
---
## AxisTickLabels::get_Rotation method


Gets or sets the rotation of the tick labels in degrees.

```cpp
int32_t Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation()
```


## Examples



Shows how to change orientation and rotation for axis tick labels. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a column chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Set axis tick label orientation and rotation.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## See Also

* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
