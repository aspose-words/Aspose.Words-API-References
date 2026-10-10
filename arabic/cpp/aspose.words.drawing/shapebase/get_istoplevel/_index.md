---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel method"
linktitle: "get_IsTopLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel method. تُرجع true إذا لم يكن هذا الشكل طفلًا لشكل مجموعة في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


إرجاع **true** إذا لم يكن هذا الشكل فرعًا لشكل مجموعة.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## أمثلة



يظهر كيفية معرفة ما إذا كان الشكل جزءًا من شكل مجموعة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// بشكل افتراضي، لا يكون الشكل جزءًا من أي شكل مجموعة، وبالتالي تكون الخاصية "IsTopLevel" مضبوطة على "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// بمجرد دمج الشكل في شكل مجموعة، تتغير الخاصية "IsTopLevel" إلى "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
