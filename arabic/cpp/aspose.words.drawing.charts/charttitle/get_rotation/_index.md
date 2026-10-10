---
title: "طريقة Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation"
linktitle: "get_Rotation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation. يحصل على أو يضبط دوران عنوان المخطط بالدرجات في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.drawing.charts/charttitle/get_rotation/
---
## ChartTitle::get_Rotation method


يحصل أو يضبط دوران عنوان المخطط بالدرجات.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation()
```


## أمثلة



يوضح كيفية ضبط الاتجاه والدوران لعناوين المخطط والمحاور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// قبل ضبط خصائص العنوان، تأكد من أن هذا العنوان سيُعرض.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## انظر أيضًا

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
