---
title: "Aspose::Words::Document::UpdateThumbnail metod"
linktitle: "UpdateThumbnail"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UpdateThumbnail metod. Uppdaterar dokumentets Thumbnail med standardalternativ i C++."
type: docs
weight: 100000
url: /sv/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Uppdaterar [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) för dokumentet med standardalternativ.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Uppdaterar [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) för dokumentet enligt de angivna alternativen.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | De genererande alternativen att använda. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
