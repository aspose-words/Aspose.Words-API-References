---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize‑metod"
linktitle: "get_ThumbnailSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize‑metod. Storleken på den genererade miniatyren i pixlar. Standard är 600x900 i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


Storlek på genererad miniatyrbild i pixlar. Standard är 600x900.

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
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
