---
title: "طريقة Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation"
linktitle: "get_Orientation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation. يحصل على أو يضبط اتجاه نص عنوان المحور في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words.drawing.charts/chartaxistitle/get_orientation/
---
## ChartAxisTitle::get_Orientation method


يسترجع أو يعيّن اتجاه نص عنوان المحور.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation()
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

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
