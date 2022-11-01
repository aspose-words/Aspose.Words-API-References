---
title: get_HorizontalRuleFormat
second_title: Aspose.Words for C++ API Reference
description: Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns null.
type: docs
weight: 131
url: /cpp/aspose.words.drawing/shape/get_horizontalruleformat/
---
## Shape.get_HorizontalRuleFormat method


Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns null.

```cpp
System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat()
```


## Examples




Shows how to insert a horizontal rule shape, and customize its formatting. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<Shape> shape = builder->InsertHorizontalRule();

SharedPtr<HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

