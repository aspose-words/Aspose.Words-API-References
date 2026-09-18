---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. Kann verwendet werden, um zusätzliche Optionen beim Erzeugen eines Vorschaubilds für ein Dokument in C++ anzugeben."
type: docs
weight: 5000
url: /de/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Kann verwendet werden, um zusätzliche Optionen beim Erzeugen einer Miniaturansicht für ein Dokument anzugeben.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Gibt an, ob ein Vorschaubild von der ersten Seite des Dokuments oder vom ersten Bild erzeugt werden soll. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Größe des erzeugten Vorschaubilds in Pixeln. Standard ist 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Setter für [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Setter für [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
