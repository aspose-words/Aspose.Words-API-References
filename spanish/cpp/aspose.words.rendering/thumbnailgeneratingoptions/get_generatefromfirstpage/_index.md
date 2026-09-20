---
title: "Método Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage"
linktitle: "get_GenerateFromFirstPage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage. Especifica si se debe generar la miniatura a partir de la primera página del documento o de la primera imagen en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Especifica si se debe generar la miniatura a partir de la primera página del documento o de la primera imagen.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
```


## Ejemplos



Muestra cómo actualizar la miniatura de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Hay dos formas de establecer una imagen de miniatura al guardar un documento en .epub.
// 1 -  Usa la primera página del documento:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Usa la primera imagen encontrada en el documento:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Ver también

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
