---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Adjustment class. يمثل قيم الضبط التي تُطبق على الشكل المحدد في C++."
type: docs
weight: 334
url: /ar/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


يمثل قيم التعديل التي تُطبق على الشكل المحدد.

```cpp
class Adjustment : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Name](./get_name/)() const | يحصل على اسم الضبط. |
| [get_Value](./get_value/)() const | يحصل أو يضبط القيمة الخام للضبط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
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
