---
title: "Aspose::Words::WatermarkType enum"
linktitle: "WatermarkType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WatermarkType enum. Anger vattenstämpeltypen i C++."
type: docs
weight: 131000
url: /sv/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Anger vattenstämpelns typ.

```cpp
enum class WatermarkType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | 0 | Indikerar att texten kommer att användas som en vattenstämpel. En sådan vattenstämpel motsvarar ett WordArt-objekt. |
| Image | 1 | Indikerar att bilden kommer att användas som en vattenstämpel. En sådan vattenstämpel motsvarar en form med bild. |
| None | 2 | Indikerar att vattenstämpeln inte är satt. |


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
