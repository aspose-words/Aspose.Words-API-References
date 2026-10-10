---
title: "طريقة Aspose::Words::Drawing::TextBox::get_VerticalAnchor"
linktitle: "get_VerticalAnchor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::TextBox::get_VerticalAnchor. تحدد المحاذاة العمودية للنص داخل الشكل في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


يحدد محاذاة النص العمودية داخل الشكل.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## ملاحظات


القيمة الافتراضية هي [Top](../../textboxanchor/).

## أمثلة



يوضح كيفية محاذاة محتوى النص داخل صندوق النص عموديًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// قم بتعيين الخاصية "VerticalAnchor" إلى "TextBoxAnchor.Top" لـ
// محاذاة النص في هذا الصندوق النصي مع الجانب العلوي للشكل.
// قم بتعيين الخاصية "VerticalAnchor" إلى "TextBoxAnchor.Middle" لـ
// محاذاة النص في هذا الصندوق النصي إلى مركز الشكل.
// قم بتعيين الخاصية "VerticalAnchor" إلى "TextBoxAnchor.Bottom" لـ
// محاذاة النص في هذا الصندوق النصي إلى أسفل الشكل.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// تتوفر محاذاة النص عموديًا داخل صناديق النص منذ Microsoft Word 2007 وما بعده.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## انظر أيضًا

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
