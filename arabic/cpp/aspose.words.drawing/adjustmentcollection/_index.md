---
title: "فئة Aspose::Words::Drawing::AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::AdjustmentCollection. تمثل مجموعة للقراءة فقط من قيم تعديل Adjustment التي تُطبق على الشكل المحدد في C++."
type: docs
weight: 667
url: /ar/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


تمثل مجموعة للقراءة فقط من قيم تعديل [Adjustment](../adjustment/) التي تُطبق على الشكل المحدد.

```cpp
class AdjustmentCollection : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد تعديلًا في الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية العمل مع القيم الأولية للتعديل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rounded rectangle shape.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(1, adjustments->get_Count());

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(u"adj", adjustment->get_Name());
ASSERT_EQ(16667, adjustment->get_Value());

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
