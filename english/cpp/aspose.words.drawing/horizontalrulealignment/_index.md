---
title: Aspose::Words::Drawing::HorizontalRuleAlignment enum
linktitle: HorizontalRuleAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::HorizontalRuleAlignment enum. Represents the alignment for the specified horizontal rule in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Represents the alignment for the specified horizontal rule.

```cpp
enum class HorizontalRuleAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | Aligned to the left. |
| Center | 1 | Aligned to the center. |
| Right | 2 | Aligned to the right. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
