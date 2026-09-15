---
title: "Aspose::Words::Drawing::ShapeBase::get_Hidden طريقة"
linktitle: "get_Hidden"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Hidden طريقة. يسترجع أو يعيّن قيمة منطقية تشير إلى ما إذا كان الشكل مرئيًا في C++."
type: docs
weight: 22750
url: /ar/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


الحصول أو تعيين قيمة منطقية تشير إلى ما إذا كان الشكل مرئيًا.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## أمثلة



يظهر كيفية إخفاء الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
