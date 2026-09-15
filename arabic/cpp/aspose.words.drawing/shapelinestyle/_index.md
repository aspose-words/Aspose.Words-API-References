---
title: "Aspose::Words::Drawing::ShapeLineStyle تعداد"
linktitle: "ShapeLineStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeLineStyle تعداد. يحدد نمط الخط المركب لشكل في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enum


يحدد نمط الخط المركب لـ [Shape](../shape/).

```cpp
enum class ShapeLineStyle
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Single | 0 | خط واحد. |
| Double | 1 | خطان مزدوجان بعرض متساوٍ. |
| ThickThin | 2 | خطان مزدوجان، أحدهما سميك والآخر رفيع. |
| ThinThick | 3 | خطان مزدوجان، أحدهما رفيع والآخر سميك. |
| Triple | 4 | ثلاثة خطوط، رفيع، سميك، رفيع. |
| Default | n/a | القيمة الافتراضية هي [Single](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
