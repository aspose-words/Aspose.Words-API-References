---
title: Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent method
linktitle: get_WidthPercent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent method. Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## Remarks


Valid values ​​range from 1 to 100 inclusive.

The default value is 100.

## Examples



Shows how to insert a horizontal rule shape, and customize its formatting. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
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
