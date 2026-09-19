---
title: "Metodo Aspose::Words::Document::UpdateThumbnail"
linktitle: "UpdateThumbnail"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::UpdateThumbnail. Aggiorna la Thumbnail del documento usando le opzioni predefinite in C++."
type: docs
weight: 100000
url: /it/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Aggiorna [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento usando le opzioni predefinite.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
```


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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Aggiorna [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento secondo le opzioni specificate.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| opzioni | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | Le opzioni di generazione da utilizzare. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
