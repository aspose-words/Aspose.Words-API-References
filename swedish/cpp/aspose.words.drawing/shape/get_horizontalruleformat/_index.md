---
title: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat metod"
linktitle: "get_HorizontalRuleFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat metod. Ger åtkomst till egenskaperna för horisontell linje-formen. För en form som inte är en horisontell linje, returneras null i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.drawing/shape/get_horizontalruleformat/
---
## Shape::get_HorizontalRuleFormat method


Tillhandahåller åtkomst till egenskaperna för den horisontella linjeformen. För en form som inte är en horisontell linje returneras **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat()
```


## Exempel



Visar hur man infogar en horisontell regelform och anpassar dess formatering.
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

## Se även

* Class [HorizontalRuleFormat](../../horizontalruleformat/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
