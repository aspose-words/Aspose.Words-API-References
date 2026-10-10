---
title: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat método"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat método. Especifica el formato en el que se guardarán las páginas o formas del documento renderizado si se utiliza este objeto de opciones de guardado. Puede ser un raster Tiff, Png, Bmp, Jpeg o un vector Emf, Eps, WebP, Svg en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardarán las páginas o formas del documento renderizado si se utiliza este objeto de opciones de guardado. Puede ser un raster [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/) o un vector [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## Observaciones


El número de otras opciones depende del formato seleccionado.

Además, es posible guardar a SVG tanto a través de [ImageSaveOptions](../) como de [SvgSaveOptions](../../svgsaveoptions/).

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
