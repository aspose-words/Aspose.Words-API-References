---
title: "Método Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality"
linktitle: "get_JpegQuality"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality método. Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento Html en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento Html.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Observaciones


Tiene efecto solo cuando un documento contiene imágenes JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes dentro de un documento al guardarlo en formato de página fija. El valor puede variar de 0 a 100, donde 0 significa la peor calidad pero máxima compresión y 100 significa la mejor calidad pero mínima compresión.

El valor predeterminado es 95.

## Ejemplos



Muestra cómo configurar la compresión al guardar un documento como JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
// para modificar la forma en que ese método renderiza el documento en una imagen.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Establezca la propiedad "JpegQuality" a "10" para usar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más prominentes.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Establezca la propiedad "JpegQuality" a "100" para usar una compresión más débil al renderizar el documento.
// Esto mejorará la calidad de la imagen a costa de un mayor tamaño de archivo.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Ver también

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
