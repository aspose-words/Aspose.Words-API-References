---
title: Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation method
linktitle: get_Orientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation method. Gets or sets the orientation of the tick label text in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


Gets or sets the orientation of the tick label text.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Remarks


The default value is [Horizontal](../../../aspose.words.drawing/shapetextorientation/).

Note that some [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) values do not affect the orientation of tick label text in value axes.

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

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
