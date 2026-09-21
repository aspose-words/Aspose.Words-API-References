---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. Kan användas för att ange ytterligare alternativ när en miniatyrbild genereras för ett dokument i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Kan användas för att ange ytterligare alternativ när en miniatyrbild för ett dokument genereras.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Anger om en miniatyrbild ska genereras från dokumentets första sida eller den första bilden. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Storlek på genererad miniatyrbild i pixlar. Standard är 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Sättare för [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Sättare för [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
