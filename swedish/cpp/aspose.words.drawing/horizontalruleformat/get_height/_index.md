---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height metod"
linktitle: "get_Height"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height metod. Hämtar eller anger höjden på den horisontella regeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Hämtar eller anger höjden på den horisontella linjen.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Anmärkningar


Detta är en genväg till egenskapen [Height](../../shapebase/get_height/).

Giltiga värden sträcker sig från 0 till 1584 inklusive.

Standardvärdet är 1,5.

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
