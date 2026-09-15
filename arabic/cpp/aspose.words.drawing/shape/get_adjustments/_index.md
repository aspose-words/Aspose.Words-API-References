---
title: "طريقة Aspose::Words::Drawing::Shape::get_Adjustments"
linktitle: "get_Adjustments"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Shape::get_Adjustments. توفر الوصول إلى القيم الأولية للتعديل لشكل. إذا كان الشكل لا يحتوي على أي قيم أولية للتعديل، تُعيد مجموعة فارغة في C++."
type: docs
weight: 3834
url: /ar/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


يوفر الوصول إلى القيم الأولية للتعديل لشكل. بالنسبة لشكل لا يحتوي على أي قيم أولية للتعديل، يعيد مجموعة فارغة.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
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

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
