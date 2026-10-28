---
title: Aspose::Words::Drawing::HorizontalRuleFormat::set_Color method
linktitle: set_Color
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::HorizontalRuleFormat::set_Color method. Sets the brush color that fills the horizontal rule in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.drawing/horizontalruleformat/set_color/
---
## HorizontalRuleFormat::set_Color method


Sets the brush color that fills the horizontal rule.

```cpp
void Aspose::Words::Drawing::HorizontalRuleFormat::set_Color(System::Drawing::Color value)
```

## Remarks


This is a shortcut to the [Color](../../fill/get_color/) property.

The default value is **Gray**. 
## Examples


Shows how to insert a horizontal rule shape, and customize its formatting.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```
## See Also

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
