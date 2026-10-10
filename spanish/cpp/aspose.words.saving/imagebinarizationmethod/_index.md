---
title: "Aspose::Words::Saving::ImageBinarizationMethod enum"
linktitle: "ImageBinarizationMethod"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageBinarizationMethod enum. Especifica el método utilizado para binarizar la imagen en C++."
type: docs
weight: 63000
url: /es/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Especifica el método utilizado para binarizar la imagen.

```cpp
enum class ImageBinarizationMethod
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Threshold | 0 | Especifica el método de umbral. |
| FloydSteinbergDithering | 1 | Especifica el tramado usando el método de difusión de error Floyd‑Steinberg. |


## Ejemplos



Muestra cómo establecer el umbral de error de binarización TIFF al usar el método Floyd‑Steinberg para renderizar una imagen TIFF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cuando guardamos el documento como TIFF, podemos pasar un objeto SaveOptions a
// ajustar el tramado que Aspose.Words aplicará al renderizar esta imagen.
// El valor predeterminado de la propiedad "ThresholdForFloydSteinbergDithering" es 128.
// Los valores más altos tienden a producir imágenes más oscuras.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
