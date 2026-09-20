---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation método"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method. Obtiene o establece un valor que determina si se debe usar GDI+ para la emulación de operaciones raster en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Obtiene o establece un valor que determina si se debe usar GDI+ para la emulación de operaciones raster o no.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Observaciones


La biblioteca Windows GDI+ podría usarse para emular operaciones raster. Proporciona soporte para todas las operaciones raster en comparación con la propia emulación de Aspose.Words, pero el rendimiento puede ser más lento en algunos casos.

Cuando este valor se establece en **true**, Aspose.Words usa GDI+ para la emulación de operaciones raster.

Cuando este valor se establece en **false**, Aspose.Words utiliza su propia implementación de la emulación de operaciones raster.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es **false**.

## Ejemplos



Muestra cómo establecer el modo de renderizado al guardar documentos con imágenes Windows Metafile a otros formatos de imagen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// determina cómo la operación de guardado procesará los Windows Metafiles en el documento.
// Si establecemos la propiedad "RenderingMode" a "MetafileRenderingMode.Vector",
// o "MetafileRenderingMode.VectorWithFallback", renderizaremos todos los metafiles como gráficos vectoriales.
// Si establecemos la propiedad "RenderingMode" a "MetafileRenderingMode.Bitmap", renderizaremos todos los metafiles como mapas de bits.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words usa GDI+ para la emulación de operaciones raster, cuando el valor se establece en true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## Ver también

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
