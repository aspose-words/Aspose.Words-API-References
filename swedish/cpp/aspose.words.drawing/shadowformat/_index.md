---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShadowFormat class. Representerar skuggformatering för ett objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Representerar skuggformatering för ett objekt. För att lära dig mer, besök dokumentationsartikeln [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class ShadowFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Rensar skuggformat. |
| [get_Color](./get_color/)() | Hämtar eller anger ett **Color**-objekt som representerar färgen för skuggan. Standardvärdet är **Black**. |
| [get_Transparency](./get_transparency/)() | Hämtar eller anger graden av transparens för skuggeffekten som ett värde mellan 0.0 (opak) och 1.0 (klar). Standardvärdet är 0.0. |
| [get_Type](./get_type/)() | Hämtar eller anger den angivna [ShadowType](../shadowtype/) för [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Returnerar **true** om formateringen som tillämpats på detta objekt är synlig. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Sättare för [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Sättare för [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man hämtar skuggfärgen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
