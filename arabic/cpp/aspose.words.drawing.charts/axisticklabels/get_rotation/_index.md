---
title: "طريقة Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation"
linktitle: "get_Rotation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation. يحصل أو يضبط دوران تسميات العلامات بالدرجات في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing.charts/axisticklabels/get_rotation/
---
## AxisTickLabels::get_Rotation method


يحصل أو يضبط دوران تسميات العلامات بالدرجات.

```cpp
int32_t Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation()
```


## أمثلة



يوضح كيفية تغيير الاتجاه والدوران لتسميات محاور العلامات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مخطط عمودي.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// عيّن اتجاه ودوران تسميات محاور العلامات.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## انظر أيضًا

* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
