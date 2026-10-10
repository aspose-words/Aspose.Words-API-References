---
title: "Aspose::Words::Document::UpdateThumbnail Methode"
linktitle: "UpdateThumbnail"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::UpdateThumbnail Methode. Aktualisiert das Thumbnail des Dokuments mit den Standardoptionen in C++."
type: docs
weight: 100000
url: /de/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Aktualisiert das [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) des Dokuments mit den Standardoptionen.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
```


## Beispiele



Zeigt, wie das Vorschaubild eines Dokuments aktualisiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Es gibt zwei Möglichkeiten, ein Vorschaubild beim Speichern eines Dokuments als .epub festzulegen.
// 1 -  Verwenden Sie die erste Seite des Dokuments:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Verwenden Sie das erste im Dokument gefundene Bild:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Aktualisiert das [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) des Dokuments gemäß den angegebenen Optionen.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | Die zu verwendenden Generierungsoptionen. |

## Beispiele



Zeigt, wie das Vorschaubild eines Dokuments aktualisiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Es gibt zwei Möglichkeiten, ein Vorschaubild beim Speichern eines Dokuments als .epub festzulegen.
// 1 -  Verwenden Sie die erste Seite des Dokuments:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Verwenden Sie das erste im Dokument gefundene Bild:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Siehe auch

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
