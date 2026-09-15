---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_IsDecorative"
linktitle: "get_IsDecorative"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_IsDecorative. يحصل على أو يعيّن العلامة التي تحدد ما إذا كان الشكل ديكوريًا في المستند في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


الحصول أو تعيين العلامة التي تحدد ما إذا كان الشكل زخرفيًا في المستند.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## أمثلة



يوضح كيفية تعيين أن الشكل ديكوري.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// إذا لم يكن "AlternativeText" فارغًا، لا يمكن أن يكون الشكل ديكوريًا.
// لهذا السبب تغيرت قيمتنا إلى 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// إنشاء شكل جديد كديكوري.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
