---
title: "Aspose::Words::ImageWatermarkOptions klass"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImageWatermarkOptions klass. Innehåller alternativ som kan specificeras när du lägger till en vattenstämpel med bild. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Innehåller alternativ som kan specificeras när du lägger till ett vattenmärke med bild. För att lära dig mer, besök artikeln [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) i dokumentationen.

```cpp
class ImageWatermarkOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Hämtar eller anger ett booleskt värde som ansvarar för tvättningseffekten av vattenstämpeln. Standardvärdet är **true**. |
| [get_Scale](./get_scale/)() const | Hämtar eller anger skalningsfaktorn uttryckt som en bråkdel av bilden. Standardvärdet är 0 - auto. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Sättare för [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Sättare för [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändra bildvattenstämpelns utseende med ett ImageWatermarkOptions-objekt,
// och skicka sedan med den när du skapar en vattenstämpel från en bildfil.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Vi har olika alternativ för att infoga en bild.
// Använd någon av följande metoder för att lägga till bildvattenstämpel.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
