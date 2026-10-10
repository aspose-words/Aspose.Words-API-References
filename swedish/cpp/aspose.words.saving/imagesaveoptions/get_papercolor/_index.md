---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor‑metoden"
linktitle: "get_PaperColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor‑metoden. Hämtar eller anger bakgrunds‑ (pappers)‑färgen för de genererade bilderna. Standardvärdet är White i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Hämtar eller anger bakgrundsfärgen (papper) för de genererade bilderna. Standardvärdet är **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Anmärkningar


När man renderar sidor i ett dokument som anger sin egen bakgrundsfärg, kommer dokumentets bakgrundsfärg att åsidosätta färgen som anges av den här egenskapen.

## Exempel



Renderar en sida i ett Word-dokument till en bild med transparent eller färgad bakgrund.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Ställ in egenskapen "PaperColor" till en transparent färg för att applicera en transparent
// bakgrund på dokumentet när det renderas till en bild.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Ställ in egenskapen "PaperColor" till en ogenomskinlig färg för att använda den färgen
// som bakgrund på dokumentet när vi renderar det till en bild.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## Se även

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
