---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage‑metod"
linktitle: "get_GenerateFromFirstPage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage‑metod. Anger om en miniatyr ska genereras från dokumentets första sida eller den första bilden i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Anger om en miniatyrbild ska genereras från dokumentets första sida eller den första bilden.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
```


## Exempel



Visar hur man uppdaterar ett dokuments miniatyrbild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Det finns två sätt att ange en miniatyrbild när ett dokument sparas till .epub.
// 1 -  Använd dokumentets första sida:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Använd den första bilden som finns i dokumentet:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Se även

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
