---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality metod"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality metod. Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG-bilderna i ett Html-dokument i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG‑bilderna i ett Html‑dokument.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Anmärkningar


Har effekt endast när ett dokument innehåller JPEG-bilder.

Använd den här egenskapen för att hämta eller ange bildkvaliteten i ett dokument när du sparar i fast sidformat. Värdet kan variera från 0 till 100 där 0 betyder sämst kvalitet men maximal komprimering och 100 betyder bästa kvalitet men minimal komprimering.

Standardvärdet är 95.

## Exempel



Visar hur man konfigurerar komprimering när man sparar ett dokument som JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Ställ in egenskapen "JpegQuality" till "10" för att använda starkare komprimering när dokumentet renderas.
// Detta kommer att minska filstorleken på dokumentet, men bilden kommer att visa mer framträdande komprimeringsartefakter.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Ställ in egenskapen "JpegQuality" till "100" för att använda svagare komprimering när dokumentet renderas.
// Detta kommer att förbättra bildkvaliteten på bekostnad av en ökad filstorlek.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Se även

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
