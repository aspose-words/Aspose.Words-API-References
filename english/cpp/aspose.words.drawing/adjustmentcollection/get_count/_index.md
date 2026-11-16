---
title: Aspose::Words::Drawing::AdjustmentCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::AdjustmentCollection::get_Count method. Gets the number of elements contained in the collection in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing/adjustmentcollection/get_count/
---
## AdjustmentCollection::get_Count method


Gets the number of elements contained in the collection.

```cpp
int32_t Aspose::Words::Drawing::AdjustmentCollection::get_Count()
```

## Examples


Shows how to work with adjustment raw values.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rounded rectangle shape.docx"));
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(adjustments->get_Count(), 1);

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(adjustment->get_Name(), u"adj");
ASSERT_EQ(adjustment->get_Value(), 16667);

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```
## See Also

* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
