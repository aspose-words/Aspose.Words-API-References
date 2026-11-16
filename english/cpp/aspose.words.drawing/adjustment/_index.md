---
title: Aspose::Words::Drawing::Adjustment class
linktitle: Adjustment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Adjustment class. Represents adjustment values that are applied to the specified shape in C++.'
type: docs
weight: 334
url: /cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Represents adjustment values that are applied to the specified shape.

```cpp
class Adjustment : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Name](./get_name/)() const | Gets the name of the adjustment. |
| [get_Value](./get_value/)() const | Gets or sets the raw value of the adjustment. |
| [set_Value](./set_value/)(int32_t) | Sets the raw value of the adjustment. |
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
