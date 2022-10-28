---
title: get_Alignment
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the alignment of the horizontal rule.
type: docs
weight: 1
url: /cpp/aspose.words.drawing/horizontalruleformat/get_alignment/
---
## HorizontalRuleFormat.get_Alignment method


Gets or sets the alignment of the horizontal rule.

```cpp
Aspose::Words::Drawing::HorizontalRuleAlignment Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment()
```


The default value is **Left**.

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

