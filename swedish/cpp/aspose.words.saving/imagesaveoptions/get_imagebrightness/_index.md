---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness metod"
linktitle: "get_ImageBrightness"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness metod. Hämtar eller anger ljusstyrkan för de genererade bilderna i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_imagebrightness/
---
## ImageSaveOptions::get_ImageBrightness method


Hämtar eller anger ljusstyrkan för de genererade bilderna.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness() const
```

## Anmärkningar


Denna egenskap har endast effekt när man sparar till rasterbildformat.

Standardvärdet är 0,5. Värdet måste ligga i intervallet mellan 0 och 1.

## Exempel



Visar hur man redigerar bilden medan Aspose.Words konverterar ett dokument till en sådan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions‑objekt till
// redigera bilden medan sparningsoperationen renderar den.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Vi kan justera dessa egenskaper för att ändra bildens ljusstyrka och kontrast.
// Båda är på en 0‑1 skala och har standardvärdet 0,5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Vi kan justera horisontell och vertikal upplösning med dessa egenskaper.
// Detta kommer att påverka bildens dimensioner.
// Standardvärdet för dessa egenskaper är 96,0, för en upplösning på 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Vi kan skala bilden med denna egenskap. Standardvärdet är 1,0, för en skalning på 100 %.
// Vi kan använda denna egenskap för att motverka eventuella förändringar i bildens dimensioner som en förändring av upplösningen skulle orsaka.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Se även

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
