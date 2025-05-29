---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words para .NET
description: Descubra la propiedad MetafileRenderingOptions de ImageSaveOptions para controlar el manejo de metarchivos en su salida renderizada para una mejor calidad de imagen.
type: docs
weight: 90
url: /es/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Permite especificar cómo se tratan los metarchivos en la salida renderizada.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Observaciones

CuandoVector Si se especifica, Aspose.Words renders metarchivo a gráficos vectoriales utilizando primero su propio motor de renderizado de metarchivos y luego renderiza gráficos vector a la imagen.

CuandoBitmap Si se especifica, Aspose.Words renderiza el metarchivo directamente en la imagen utilizando el motor de renderizado de metarchivos GDI+.

El motor de renderizado de metarchivos GDI+ funciona más rápido y admite casi todas las funciones de los metarchivos, pero en resoluciones bajas puede generar resultados inconsistentes en comparación con el resto de los gráficos vectoriales (especialmente para texto) de la página. El motor de renderizado de metarchivos Aspose.Words produce resultados más consistentes incluso en resoluciones bajas, pero funciona más lento y puede generar metarchivos complejos de forma imprecisa.

El valor predeterminado para[`MetafileRenderingMode`](../../metafilerenderingmode/) esBitmap.

## Ejemplos

Muestra cómo configurar el modo de renderizado al guardar documentos con imágenes de Metarchivo de Windows en otros formatos de imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// determina cómo la operación de guardado procesará los metarchivos de Windows en el documento.
// Si establecemos la propiedad "RenderingMode" en "MetafileRenderingMode.Vector",
// o "MetafileRenderingMode.VectorWithFallback", renderizaremos todos los metarchivos como gráficos vectoriales.
// Si establecemos la propiedad "RenderingMode" en "MetafileRenderingMode.Bitmap", renderizaremos todos los metarchivos como mapas de bits.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words usa GDI+ para la emulación de operaciones raster, cuando el valor se establece en verdadero.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Ver también

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
