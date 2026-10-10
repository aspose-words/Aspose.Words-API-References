---
title: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions konstruktor"
linktitle: "ImageSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions konstruktor. Initierar en ny instans av denna klass som kan användas för att spara renderade bilder i Tiff-, Png-, Bmp-, Jpeg-, Emf-, Eps-, WebP- eller Svg-format i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


Initierar en ny instans av den här klassen som kan användas för att spara renderade bilder i formatet [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../) eller [Svg](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kan vara i formatet [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/)[WebP](../) eller [Svg](../../../aspose.words/saveformat/) format. |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
