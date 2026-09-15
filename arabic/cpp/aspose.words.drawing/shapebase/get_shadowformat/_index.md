---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_ShadowFormat"
linktitle: "get_ShadowFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_ShadowFormat. يجلب تنسيق الظل للشكل في C++."
type: docs
weight: 47000
url: /ar/cpp/aspose.words.drawing/shapebase/get_shadowformat/
---
## ShapeBase::get_ShadowFormat method


يحصل على تنسيق الظل للشكل.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> Aspose::Words::Drawing::ShapeBase::get_ShadowFormat()
```


## أمثلة



يوضح كيفية الحصول على لون الظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## انظر أيضًا

* Class [ShadowFormat](../../shadowformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
