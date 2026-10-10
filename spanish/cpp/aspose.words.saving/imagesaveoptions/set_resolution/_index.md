---
title: "Método Aspose::Words::Saving::ImageSaveOptions::set_Resolution"
linktitle: "set_Resolution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::ImageSaveOptions::set_Resolution. Establece tanto la resolución horizontal como la vertical para las imágenes generadas, en puntos por pulgada en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Establece tanto la resolución horizontal como la vertical para las imágenes generadas, en puntos por pulgada.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Observaciones


Esta propiedad tiene efecto solo al guardar en formatos de imagen raster.

## Ejemplos



Muestra cómo especificar una resolución al renderizar un documento a PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
// para modificar la forma en que ese método renderiza el documento en una imagen.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Establezca la propiedad "Resolution" a "72" para renderizar el documento a 72dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Establezca la propiedad "Resolution" a "300" para renderizar el documento a 300dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Ver también

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
