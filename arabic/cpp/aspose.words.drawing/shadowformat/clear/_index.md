---
title: "طريقة Aspose::Words::Drawing::ShadowFormat::Clear"
linktitle: "Clear"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShadowFormat::Clear. تقوم بمسح تنسيق الظل في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


يمسح تنسيق الظل.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
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
