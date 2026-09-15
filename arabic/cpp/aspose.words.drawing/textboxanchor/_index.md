---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. يحدد القيم المستخدمة لمحاذاة النص العمودي في الشكل بلغة C++."
type: docs
weight: 39000
url: /ar/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


يحدد القيم المستخدمة لمحاذاة النص العمودي داخل الشكل.

```cpp
enum class TextBoxAnchor
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أعلى | 0 | النص محاذى إلى أعلى صندوق النص. |
| Middle | 1 | النص محاذى إلى وسط صندوق النص. |
| أسفل | 2 | النص محاذى إلى أسفل صندوق النص. |
| TopCentered | 3 | النص محاذى إلى أعلى مركز في صندوق النص. |
| MiddleCentered | 4 | النص محاذى إلى وسط مركز في صندوق النص. |
| BottomCentered | 5 | النص محاذى إلى أسفل مركز في صندوق النص. |
| TopBaseline | 6 | النص محاذى إلى الخط الأساسي العلوي في صندوق النص. |
| BottomBaseline | 7 | النص محاذى إلى الخط الأساسي السفلي في صندوق النص. |
| TopCenteredBaseline | 8 | النص مُحاذى إلى الخط الأساسي المركزي العلوي لصندوق النص. |
| BottomCenteredBaseline | 9 | النص مُحاذى إلى الخط الأساسي المركزي السفلي لصندوق النص. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
