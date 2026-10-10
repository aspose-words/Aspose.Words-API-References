---
title: "Aspose::Words::Drawing::HorizontalRuleFormat class"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::HorizontalRuleFormat-klass. Representerar formatering av horisontell linje. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Representerar formatering av horisontell linje. För att lära dig mer, besök dokumentationsartikeln [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Hämtar eller anger justeringen av den horisontella linjen. |
| [get_Color](./get_color/)() | Hämtar eller anger penselfärgen som fyller den horisontella linjen. |
| [get_Height](./get_height/)() | Hämtar eller anger höjden på den horisontella linjen. |
| [get_NoShade](./get_noshade/)() | Anger närvaron av 3D-skuggning för den horisontella linjen. Om **true** är den horisontella linjen utan 3D-skuggning och en solid färg används. |
| [get_WidthPercent](./get_widthpercent/)() | Hämtar eller anger längden på den specificerade horisontella linjen uttryckt som en procentandel av fönstrets bredd. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Sättare för [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Sättare för [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Sättare för [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Sättare för [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
