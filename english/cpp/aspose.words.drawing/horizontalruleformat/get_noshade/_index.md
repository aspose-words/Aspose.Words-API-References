---
title: Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade method
linktitle: get_NoShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade method. Indicates the presence of 3D shading for the horizontal rule. If true, then the horizontal rule is without 3D shading and solid color is used in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Indicates the presence of 3D shading for the horizontal rule. If **true**, then the horizontal rule is without 3D shading and solid color is used.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Remarks


The default value is **false**.

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
