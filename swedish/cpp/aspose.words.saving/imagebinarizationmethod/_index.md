---
title: "Aspose::Words::Saving::ImageBinarizationMethod enum"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageBinarizationMethod enum. Anger metoden som används för att binarisera bild i C++."
type: docs
weight: 63000
url: /sv/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Anger metoden som används för att binarisera bilden.

```cpp
enum class ImageBinarizationMethod
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Threshold | 0 | Anger tröskelmetod. |
| FloydSteinbergDithering | 1 | Anger dithering med Floyd‑Steinberg felspredningsmetod. |


## Exempel



Visar hur man ställer in TIFF-binariseringsfeltröskeln när man använder Floyd‑Steinberg‑metoden för att rendera en TIFF‑bild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// När vi sparar dokumentet som en TIFF kan vi skicka ett SaveOptions‑objekt till
// justera den dithering som Aspose.Words kommer att tillämpa när bilden renderas.
// Standardvärdet för egenskapen "ThresholdForFloydSteinbergDithering" är 128.
// Högre värden tenderar att producera mörkare bilder.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
