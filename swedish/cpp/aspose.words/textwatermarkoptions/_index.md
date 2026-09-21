---
title: "Aspose::Words::TextWatermarkOptions klass"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextWatermarkOptions-klass. Innehåller alternativ som kan specificeras när man lägger till ett vattenstämpel med text. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 72000
url: /sv/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Innehåller alternativ som kan specificeras när en vattenstämpel med text läggs till. För att läsa mer, besök [Arbeta med vattenstämpel](https://docs.aspose.com/words/cpp/working-with-watermark/) dokumentationsartikel.

```cpp
class TextWatermarkOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Color](./get_color/)() const | Hämtar eller anger teckensnittsfärg. Standardvärdet är **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Hämtar eller anger teckensnittsfamiljens namn. Standardvärdet är "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Hämtar eller anger en teckensnittsstorlek. Standardvärdet är 0 – auto. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Hämtar eller anger ett booleskt värde som ansvarar för vattenstämpelns opacitet. Standardvärdet är **true**. |
| [get_Layout](./get_layout/)() const | Hämtar eller anger layout för vattenstämpeln. Standardvärdet är [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | Sättare för [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | Sättare för [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Sättare för [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Sättare för [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
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
