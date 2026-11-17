---
title: Aspose::Words::Drawing::AdjustmentCollection class
linktitle: AdjustmentCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::AdjustmentCollection class. Represents a read-only collection of Adjustment adjust values that are applied to the specified shape in C++.'
type: docs
weight: 667
url: /cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Represents a read-only collection of [Adjustment](../adjustment/) adjust values that are applied to the specified shape.

```cpp
class AdjustmentCollection : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [idx_get](./idx_get/)(int32_t) | Returns an adjustment at the specified index. |
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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
