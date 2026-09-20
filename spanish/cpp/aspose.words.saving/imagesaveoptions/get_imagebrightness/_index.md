---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness método"
linktitle: "get_ImageBrightness"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness método. Obtiene o establece el brillo de las imágenes generadas en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_imagebrightness/
---
## ImageSaveOptions::get_ImageBrightness method


Obtiene o establece el brillo para las imágenes generadas.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness() const
```

## Observaciones


Esta propiedad tiene efecto solo al guardar en formatos de imagen raster.

El valor predeterminado es 0.5. El valor debe estar en el rango entre 0 y 1.

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
