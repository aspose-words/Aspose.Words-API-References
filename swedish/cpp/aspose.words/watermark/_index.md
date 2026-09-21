---
title: "Aspose::Words::Watermark-klass"
linktitle: "Vattenstämpel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Watermark-klass. Representerar en klass för att arbeta med dokumentets vattenstämpel. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 76000
url: /sv/cpp/aspose.words/watermark/
---
## Watermark class


Representerar en klass för att arbeta med dokumentvattenstämpel. För att lära dig mer, besök artikeln [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) i dokumentationen.

```cpp
class Watermark : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Type](./get_type/)() | Hämtar vattenstämpeltypen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort vattenstämpeln. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Lägger till bildvattenstämpel i dokumentet. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Lägger till bildvattenstämpel i dokumentet. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Lägger till bildvattenstämpel i dokumentet. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Lägger till bildvattenstämpel i dokumentet. |
| [SetText](./settext/)(const System::String\&) | Lägger till textvattenstämpel i dokumentet. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Lägger till textvattenstämpel i dokumentet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man skapar ett textvattenstämpel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Lägg till ett vattenmärke i klartext.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Om vi vill redigera textformateringen genom att använda den som ett vattenmärke,
// kan vi göra det genom att skicka ett TextWatermarkOptions-objekt när vi skapar vattenmärket.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Vi kan ta bort ett vattenmärke från ett dokument på detta sätt.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
