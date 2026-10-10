---
title: "Aspose::Words::FrameFormat klass"
linktitle: "FrameFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FrameFormat klass. Representerar ramrelaterad formatering för ett stycke i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words/frameformat/
---
## FrameFormat class


Representerar ramrelaterad formatering för ett stycke.

```cpp
class FrameFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Height](./get_height/)() | Hämtar höjden på den angivna ramen. |
| [get_HeightRule](./get_heightrule/)() | Hämtar regeln för att bestämma höjden på den angivna ramen. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Hämtar horisontell justering av den angivna ramen. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Hämtar horisontellt avstånd mellan en ram och den omgivande texten, i punkter. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Hämtar horisontellt avstånd mellan ramens kant och det objekt som anges av egenskapen [RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [get_IsFrame](./get_isframe/)() | Returnerar **true** om stycket är en ram. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Hämtar den relativa horisontella positionen för en ram. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Hämtar den relativa vertikala positionen för en ram. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Hämtar vertikal justering av den angivna ramen. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Anger vertikalt avstånd (i punkter) mellan en ram och den omgivande texten. |
| [get_VerticalPosition](./get_verticalposition/)() | Hämtar vertikalt avstånd mellan ramens kant och det objekt som anges av egenskapen [RelativeVerticalPosition](./get_relativeverticalposition/). |
| [get_Width](./get_width/)() | Hämtar bredden på den angivna ramen, i punkter. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


Detta objekt skapas alltid. Om ett stycke är en ram kommer alla egenskaper att innehålla respektive värden, annars sätts alla egenskaper till sina standardvärden.

Använd [IsFrame](./get_isframe/) för att kontrollera om stycket är en ram.

## Exempel



Visar hur man hämtar information om formateringsegenskaper för stycken som är ramar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraph frame.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::Drawing::HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(Aspose::Words::Drawing::VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
