---
title: "طريقة Aspose::Words::Drawing::Shape::get_FillColor"
linktitle: "get_FillColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Shape::get_FillColor. تحدد لون الفرشاة الذي يملأ المسار المغلق للشكل في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing/shape/get_fillcolor/
---
## Shape::get_FillColor method


يحدد لون الفرشاة الذي يملأ المسار المغلق للشكل.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_FillColor()
```

## ملاحظات


هذا اختصار إلى الخاصية [Color](../../fill/get_color/).

القيمة الافتراضية هي **White**.

## أمثلة



يعرض كيفية تعبئة شكل بلون صلب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// اكتب بعض النص، ثم غطه بشكل عائم.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// استخدم خاصية "StrokeColor" لتعيين لون حدود الشكل.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// خاصية "Opacity" تحدد مدى شفافية اللون على مقياس من 0 إلى 1،
// حيث يكون 1 غير شفاف تمامًا، و0 غير مرئي.
// ملء الشكل بشكل افتراضي غير شفاف تمامًا، لذا لا يمكننا رؤية النص الذي يقع فوقه هذا الشكل.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// قم بتعيين شفافية لون ملء الشكل إلى قيمة أقل حتى نتمكن من رؤية النص تحته.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## انظر أيضًا

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
