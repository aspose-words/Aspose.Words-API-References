---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. Puede usarse para especificar opciones adicionales al generar una miniatura para un documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Puede usarse para especificar opciones adicionales al generar una miniatura de un documento.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Especifica si se debe generar la miniatura a partir de la primera página del documento o de la primera imagen. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Tamaño de la miniatura generada en píxeles. El valor predeterminado es 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Establecedor para [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Establecedor para [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
