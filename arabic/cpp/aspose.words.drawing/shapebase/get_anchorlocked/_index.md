---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_AnchorLocked"
linktitle: "get_AnchorLocked"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_AnchorLocked. تحدد ما إذا كان مرساة الشكل مقفلة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


يحدد ما إذا كان مرساة الشكل مقفلة.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## ملاحظات


القيمة الافتراضية هي **false**.

يؤثر فقط على الأشكال ذات المستوى الأعلى.

هذه الخاصية تؤثر على سلوك مرساة الشكل في Microsoft Word. عندما لا تكون المرساة مقفلة، يمكن أن يؤدي تحريك الشكل في Microsoft Word إلى تحريك مرساة الشكل أيضًا.

## أمثلة



يوضح كيفية قفل أو إلغاء قفل مرساة الفقرة الخاصة بالشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// قم بتعيين الخاصية \"AnchorLocked\" إلى \"true\" لمنع مرساة الشكل
// من التحرك عند تحريك الشكل في Microsoft Word.
// قم بتعيين الخاصية \"AnchorLocked\" إلى \"false\" للسماح بأي حركة للشكل
// ولتتحرك مرساها أيضًا إلى أي فقرة أخرى يقترب منها الشكل.
shape->set_AnchorLocked(anchorLocked);

// إذا لم يكن للشكل رمز مرساة مرئي إلى يساره،
// سنحتاج إلى تمكين المراسي المرئية عبر "Options" -> "Display" -> "Object Anchors".
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
