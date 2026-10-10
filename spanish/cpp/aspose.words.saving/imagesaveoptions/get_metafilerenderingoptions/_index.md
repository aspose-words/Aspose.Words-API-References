---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions método"
linktitle: "get_MetafileRenderingOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions método. Permite especificar cómo se tratan los metarchivos en la salida renderizada en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Permite especificar cómo se tratan los metaficheros en la salida renderizada.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Observaciones


Cuando se especifica [Vector](../../metafilerenderingmode/), Aspose.Words renderiza el metarchivo a gráficos vectoriales usando primero su propio motor de renderizado de metarchivos y luego renderiza los gráficos vectoriales a la imagen.

Cuando se especifica [Bitmap](../../metafilerenderingmode/), Aspose.Words renderiza el metarchivo directamente a la imagen usando el motor de renderizado de metarchivos GDI+.

El motor de renderizado de metarchivos GDI+ funciona más rápido, admite casi todas las características de los metarchivos pero en resoluciones bajas puede producir resultados inconsistentes en comparación con el resto de los gráficos vectoriales (especialmente el texto) en la página. El motor de renderizado de metarchivos de Aspose.Words producirá resultados más consistentes incluso en resoluciones bajas, pero funciona más lento y puede renderizar de forma inexacta metarchivos complejos.

El valor predeterminado para [MetafileRenderingMode](../../metafilerenderingmode/) es [Bitmap](../../metafilerenderingmode/).

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

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
