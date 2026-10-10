---
title: "Aspose::Words::Drawing::ShapeBase::get_Title طريقة"
linktitle: "get_Title"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Title طريقة. يحصل على أو يضبط العنوان (التسمية) لكائن الشكل الحالي في C++."
type: docs
weight: 51000
url: /ar/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


يحصل أو يضبط العنوان (التسمية) لكائن الشكل الحالي.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## ملاحظات


القيمة الافتراضية هي سلسلة فارغة.

لا يمكن أن يكون **null**، لكنه يمكن أن يكون سلسلة فارغة.

## أمثلة



يعرض كيفية ضبط عنوان الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أنشئ شكلاً، أعطه عنوانًا، ثم أضفه إلى المستند.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// عند حفظ مستند يحتوي على شكل له عنوان،
// ستقوم Aspose.Words بتخزين ذلك العنوان في النص البديل للشكل.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
