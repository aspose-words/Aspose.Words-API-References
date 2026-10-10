---
title: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution metod"
linktitle: "set_Resolution"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution metod. Anger både horisontell och vertikal upplösning för de genererade bilderna, i punkter per tum i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Anger både horisontell och vertikal upplösning för de genererade bilderna, i punkter per tum.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Anmärkningar


Denna egenskap har endast effekt när man sparar till rasterbildformat.

## Exempel



Visar hur man specificerar en upplösning när man renderar ett dokument till PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Ställ in egenskapen "Resolution" till "72" för att rendera dokumentet i 72 dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Ställ in egenskapen "Resolution" till "300" för att rendera dokumentet i 300 dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Se även

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
