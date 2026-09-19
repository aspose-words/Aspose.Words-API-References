---
title: "Metodo Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage"
linktitle: "get_GenerateFromFirstPage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage. Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
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

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
