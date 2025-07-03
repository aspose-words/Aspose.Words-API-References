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
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Setter for [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
| static [Type](./type/)() |  |

## Examples



Shows how to work with adjustment raw values. 
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

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
