---
title: Aspose::Words::Drawing::HorizontalRuleFormat::set_Height method
linktitle: set_Height
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::HorizontalRuleFormat::set_Height method. Sets the height of the horizontal rule in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.drawing/horizontalruleformat/set_height/
---
## HorizontalRuleFormat::set_Height method


Sets the height of the horizontal rule.

```cpp
void Aspose::Words::Drawing::HorizontalRuleFormat::set_Height(double value)
```

## Remarks


This is a shortcut to the [Height](../../shapebase/get_height/) property.

Valid values ​​range from 0 to 1584 inclusive.

The default value is 1.5.
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
## Exceptions

* **ArgumentOutOfRangeException** -  Throws when argument was out of the range of valid values.

## See Also

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
