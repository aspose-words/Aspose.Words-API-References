---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize metod"
linktitle: "get_ImageSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize metod. Hämtar eller anger storleken på en genererad bild i pixlar i C++."
type: docs
weight: 7500
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Hämtar eller anger storleken på en genererad bild i pixlar.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Anmärkningar


Denna egenskap har endast effekt när man sparar till rasterbildformat.

Standardvärdet är (0 x 0), vilket betyder att storleken på den genererade bilden beräknas enligt bildens storlek i punkter, den angivna upplösningen och skalan.

## Exempel



Visar hur man renderar varje sida i ett dokument till en separat TIFF-bild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Ställ in egenskapen "PageSet" till numret på den första sidan från
    // vilken man ska börja rendera dokumentet från.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exportera sidan med 2325x5325 pixlar och 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## Se även

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
