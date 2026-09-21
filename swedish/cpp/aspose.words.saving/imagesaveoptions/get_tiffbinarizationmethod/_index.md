---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod metod"
linktitle: "get_TiffBinarizationMethod"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod metod. Hämtar eller anger metod som används vid konvertering av bilder till 1 bpp-format när SaveFormat är Tiff och TiffCompression är lika med Ccitt3 eller Ccitt4 i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Hämtar eller anger metod som används vid konvertering av bilder till 1 bpp-format när [SaveFormat](../get_saveformat/) är [Tiff](../../../aspose.words/saveformat/) och [TiffCompression](../get_tiffcompression/) är lika med [Ccitt3](../../tiffcompression/) eller [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Anmärkningar


Standardvärdet är [Threshold](../../imagebinarizationmethod/).

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
