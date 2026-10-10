---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color metod"
linktitle: "get_Color"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color metod. Hämtar eller anger penselfärgen som fyller den horisontella linjen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/horizontalruleformat/get_color/
---
## HorizontalRuleFormat::get_Color method


Hämtar eller anger penselfärgen som fyller den horisontella linjen.

```cpp
System::Drawing::Color Aspose::Words::Drawing::HorizontalRuleFormat::get_Color()
```

## Anmärkningar


Detta är en genväg till egenskapen [Color](../../fill/get_color/).

Standardvärdet är **Gray**.

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

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
