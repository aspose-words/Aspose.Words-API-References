---
title: "طريقة Aspose::Words::Drawing::Stroke::get_JoinStyle"
linktitle: "get_JoinStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Stroke::get_JoinStyle. يحدد نمط الوصل لخط متعدد النقاط في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.drawing/stroke/get_joinstyle/
---
## Stroke::get_JoinStyle method


يحدد نمط الانضمام للخط المتعدد.

```cpp
Aspose::Words::Drawing::JoinStyle Aspose::Words::Drawing::Stroke::get_JoinStyle()
```

## ملاحظات


القيمة الافتراضية هي [Round](../../joinstyle/).

## أمثلة



يظهر كيفية تغيير خصائص الحد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// الأشكال الأساسية، مثل المستطيل، لها جزآن مرئيان.
// 1 -  التعبئة، التي تُطبق على المنطقة داخل حدود الشكل:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  الحد، الذي يحدد حدود الشكل:
// تعديل خصائص مختلفة لحد هذا الشكل.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## انظر أيضًا

* Enum [JoinStyle](../../joinstyle/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
