---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod método"
linktitle: "get_TiffBinarizationMethod"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod método. Obtiene o establece el método usado al convertir imágenes a formato de 1 bpp cuando SaveFormat es Tiff y TiffCompression es igual a Ccitt3 o Ccitt4 en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Obtiene o establece el método usado al convertir imágenes a formato de 1 bpp cuando [SaveFormat](../get_saveformat/) es [Tiff](../../../aspose.words/saveformat/) y [TiffCompression](../get_tiffcompression/) es igual a [Ccitt3](../../tiffcompression/) o [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Observaciones


El valor predeterminado es [Threshold](../../imagebinarizationmethod/).

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
