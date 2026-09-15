---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_AlternativeText"
linktitle: "get_AlternativeText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_AlternativeText. يحدد النص البديل الذي يُعرض بدلاً من الرسم البياني في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/shapebase/get_alternativetext/
---
## ShapeBase::get_AlternativeText method


يحدد النص البديل الذي يُعرض بدلاً من الرسم.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_AlternativeText()
```

## ملاحظات


القيمة الافتراضية هي سلسلة فارغة.

## أمثلة



يظهر كيفية استخدام النص البديل للشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// يمكننا الوصول إلى النص البديل لشكل ما بالنقر بزر الماوس الأيمن عليه، ثم عبر "Format AutoShape" -> "Alt Text".
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// احفظ المستند كملف HTML، ثم احذف الصورة المرتبطة التي تنتمي إلى شكلنا.
// المتصفح الذي يقرأ ملف HTML الخاص بنا سيعرض النص البديل مكان الصورة المفقودة.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
