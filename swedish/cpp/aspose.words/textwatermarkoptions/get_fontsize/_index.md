---
title: "Aspose::Words::TextWatermarkOptions::get_FontSize metod"
linktitle: "get_FontSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextWatermarkOptions::get_FontSize metod. Hämtar eller anger en teckenstorlek. Standardvärdet är 0 – auto i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/textwatermarkoptions/get_fontsize/
---
## TextWatermarkOptions::get_FontSize method


Hämtar eller anger en teckensnittsstorlek. Standardvärdet är 0 – auto.

```cpp
float Aspose::Words::TextWatermarkOptions::get_FontSize() const
```

## Anmärkningar


Giltiga värden ligger mellan 0 och 65.5 inklusive.

Automatisk teckenstorlek betyder att vattenstämpeln skalas till sin maximala bredd och maximala höjd i förhållande till sidmarginalerna.

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

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
