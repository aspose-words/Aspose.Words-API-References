---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words para .NET
description: Descubra la propiedad MetafileRenderingOptions UseGdiRasterOperationsEmulation para optimizar las operaciones ráster con GDI. ¡Mejore el rendimiento y la flexibilidad hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Obtiene o establece un valor que determina si se debe utilizar o no GDI+ para la emulación de operaciones ráster.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Observaciones

La biblioteca GDI+ de Windows permite emular operaciones ráster. Ofrece compatibilidad con todas las operaciones ráster `operation `, a diferencia de la emulación propia de Aspose.Words, pero el rendimiento puede ser menor en algunos casos.

Cuando este valor se establece en`verdadero`Aspose.Words utiliza GDI+ para la emulación de operaciones raster.

Cuando este valor se establece en`FALSO`Aspose.Words utiliza su propia implementación de emulación de operaciones raster.

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`FALSO`.

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

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
