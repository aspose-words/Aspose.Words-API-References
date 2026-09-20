---
title: "Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution método"
linktitle: "get_HorizontalResolution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution método. Obtiene o establece la resolución horizontal para las imágenes generadas, en puntos por pulgada en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_horizontalresolution/
---
## ImageSaveOptions::get_HorizontalResolution method


Obtiene o establece la resolución horizontal para las imágenes generadas, en puntos por pulgada.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution() const
```

## Observaciones


Esta propiedad solo tiene efecto al guardar en formatos de imagen raster y afecta el tamaño de salida en píxeles.

El valor predeterminado es 96.

## Ejemplos



Muestra cómo editar la imagen mientras Aspose.Words convierte un documento a una.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// edita la imagen mientras la operación de guardado la renderiza.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Podemos ajustar estas propiedades para cambiar el brillo y el contraste de la imagen.
// Ambas están en una escala de 0-1 y su valor predeterminado es 0.5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Podemos ajustar la resolución horizontal y vertical con estas propiedades.
// Esto afectará las dimensiones de la imagen.
// El valor predeterminado para estas propiedades es 96.0, para una resolución de 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Podemos escalar la imagen usando esta propiedad. El valor predeterminado es 1.0, para un escalado del 100%.
// Podemos usar esta propiedad para anular cualquier cambio en las dimensiones de la imagen que causaría cambiar la resolución.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Ver también

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
