---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. Può essere usato per specificare opzioni aggiuntive durante la generazione di una miniatura per un documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Può essere usato per specificare opzioni aggiuntive durante la generazione di una miniatura per un documento.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Dimensione della miniatura generata in pixel. Il valore predefinito è 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Impostatore per [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Impostatore per [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come aggiornare la miniatura di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Esistono due modi per impostare un'immagine miniatura quando si salva un documento in .epub.
// 1 -  Usa la prima pagina del documento:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Usa la prima immagine trovata nel documento:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Vedi anche

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
