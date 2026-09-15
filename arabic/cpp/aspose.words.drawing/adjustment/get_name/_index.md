---
title: "Aspose::Words::Drawing::Adjustment::get_Name طريقة"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Adjustment::get_Name طريقة. يحصل على اسم التعديل في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing/adjustment/get_name/
---
## Adjustment::get_Name method


يحصل على اسم الضبط.

```cpp
System::String Aspose::Words::Drawing::Adjustment::get_Name() const
```


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

* Class [Adjustment](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
