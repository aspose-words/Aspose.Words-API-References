---
title: "Aspose::Words::ImageWatermarkOptions::get_Scale metod"
linktitle: "get_Scale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImageWatermarkOptions::get_Scale metod. Hämtar eller anger skalningsfaktorn uttryckt som en bråkdel av bilden. Standardvärdet är 0 – auto i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Hämtar eller anger skalningsfaktorn uttryckt som en bråkdel av bilden. Standardvärdet är 0 - auto.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Anmärkningar


Giltiga värden ligger mellan 0 och 65.5 inklusive.

Automatisk skalning innebär att vattenstämpeln skalas till sin maximala bredd och maximala höjd i förhållande till sidmarginalerna.

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

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
