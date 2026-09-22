---
title: "طريقة Aspose::Words::Drawing::ShadowFormat::get_Visible"
linktitle: "get_Visible"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShadowFormat::get_Visible. تُرجع true إذا كان التنسيق المطبق على هذه الحالة مرئيًا في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/shadowformat/get_visible/
---
## ShadowFormat::get_Visible method


يرجع **true** إذا كان التنسيق المطبق على هذه الحالة مرئيًا.

```cpp
bool Aspose::Words::Drawing::ShadowFormat::get_Visible()
```


## أمثلة



يعرض كيفية العمل مع تنسيق الظل للشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## انظر أيضًا

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
