---
title: Aspose::Words::Drawing::Adjustment::set_Value method
linktitle: set_Value
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Adjustment::set_Value method. Sets the raw value of the adjustment in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/adjustment/set_value/
---
## Adjustment::set_Value method


Sets the raw value of the adjustment.

```cpp
void Aspose::Words::Drawing::Adjustment::set_Value(int32_t value)
```

## Remarks

 An adjust value is simply a guide that has a value based formula specified. That is, no calculation takes place for an adjust value guide. Instead, this guide specifies a parameter value that is used for calculations within the shape guides. 
## Examples


Shows how to work with adjustment raw values.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rounded rectangle shape.docx"));
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(1, adjustments->get_Count());

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(u"adj", adjustment->get_Name());
ASSERT_EQ(16667, adjustment->get_Value());

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```
## See Also

* Class [Adjustment](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
