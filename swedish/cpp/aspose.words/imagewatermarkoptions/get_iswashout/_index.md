---
title: "Aspose::Words::ImageWatermarkOptions::get_IsWashout metod"
linktitle: "get_IsWashout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImageWatermarkOptions::get_IsWashout metod. Hämtar eller anger ett booleskt värde som ansvarar för tvättningseffekten av vattenstämpeln. Standardvärdet är true i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Hämtar eller anger ett booleskt värde som ansvarar för tvättningseffekten av vattenstämpeln. Standardvärdet är **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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
