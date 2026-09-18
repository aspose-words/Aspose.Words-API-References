---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage Methode"
linktitle: "get_GenerateFromFirstPage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage Methode. Gibt an, ob das Miniaturbild aus der ersten Seite des Dokuments oder dem ersten Bild in C++ erzeugt werden soll."
type: docs
weight: 3000
url: /de/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Gibt an, ob ein Vorschaubild von der ersten Seite des Dokuments oder vom ersten Bild erzeugt werden soll.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
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

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
