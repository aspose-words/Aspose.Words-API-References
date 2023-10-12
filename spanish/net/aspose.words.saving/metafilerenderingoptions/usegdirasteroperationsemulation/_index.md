---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
second_title: Referencia de API de Aspose.Words para .NET
description: MetafileRenderingOptions propiedad. Obtiene o establece un valor que determina si se utiliza o no GDI para la emulación de operaciones ráster.
type: docs
weight: 80
url: /es/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Obtiene o establece un valor que determina si se utiliza o no GDI+ para la emulación de operaciones ráster.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

### Observaciones

La biblioteca Windows GDI+ podría usarse para emular operaciones ráster. Proporciona soporte para todas las operaciones ráster en comparación con la propia emulación de Aspose.Words, pero el rendimiento puede ser más lento en algunos casos.

Cuando este valor se establece en`verdadero`, Aspose.Words usa GDI+ para la emulación de operaciones ráster.

Cuando este valor se establece en`FALSO`, Aspose.Words utiliza su propia implementación de emulación de operaciones ráster.

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`FALSO`.

### Ejemplos

Muestra cómo configurar el modo de representación al guardar documentos con imágenes de metarchivo de Windows en otros formatos de imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// determina cómo la operación de guardado procesará los metarchivos de Windows en el documento.
// Si configuramos la propiedad "RenderingMode" en "MetafileRenderingMode.Vector",
// o "MetafileRenderingMode.VectorWithFallback", representaremos todos los metarchivos como gráficos vectoriales.
// Si configuramos la propiedad "RenderingMode" en "MetafileRenderingMode.Bitmap", representaremos todos los metarchivos como mapas de bits.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words usa GDI+ para la emulación de operaciones ráster, cuando el valor se establece en verdadero.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Ver también

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../metafilerenderingoptions/)
* asamblea [Aspose.Words](../../../)


