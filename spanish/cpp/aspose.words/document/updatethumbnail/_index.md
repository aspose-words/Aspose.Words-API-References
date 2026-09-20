---
title: "Aspose::Words::Document::UpdateThumbnail método"
linktitle: "UpdateThumbnail"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::UpdateThumbnail método. Actualiza Thumbnail del documento usando opciones predeterminadas en C++."
type: docs
weight: 100000
url: /es/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Actualiza [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento usando opciones predeterminadas.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Actualiza [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento según las opciones especificadas.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| opciones | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | Las opciones de generación a usar. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
