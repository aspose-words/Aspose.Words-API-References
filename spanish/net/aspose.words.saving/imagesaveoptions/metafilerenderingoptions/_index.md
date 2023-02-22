---
title: ImageSaveOptions.MetafileRenderingOptions
second_title: Referencia de API de Aspose.Words para .NET
description: ImageSaveOptions propiedad. Permite especificar cómo se tratan los metarchivos en la salida renderizada.
type: docs
weight: 80
url: /es/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Permite especificar cómo se tratan los metarchivos en la salida renderizada.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

### Observaciones

CuandoVector se especifica, Aspose.Words renderiza el metarchivo en gráficos vectoriales utilizando primero su propio motor de renderizado de metarchivos y luego renderiza los gráficos vectoriales en la imagen.

CuandoBitmap se especifica, Aspose.Words renderiza el metarchivo directamente en la imagen mediante el motor de renderizado de metarchivos GDI+.

El motor de representación de metarchivos GDI+ funciona más rápido, es compatible con casi todas las funciones de metarchivos, pero en resoluciones low puede producir resultados inconsistentes en comparación con el resto de gráficos vectoriales (especialmente para texto) en la página. El motor de procesamiento de metarchivos de Aspose.Words producirá resultados más consistentes even en resoluciones bajas, pero funciona más lentamente y puede generar metarchivos complejos de manera imprecisa.

El valor predeterminado para[`MetafileRenderingMode`](../../metafilerenderingmode/) esBitmap.

### Ejemplos

Muestra cómo configurar el modo de representación al guardar documentos con imágenes de metarchivo de Windows en otros formatos de imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// determinar cómo la operación de guardado procesará los metarchivos de Windows en el documento.
// Si establecemos la propiedad "RenderingMode" en "MetafileRenderingMode.Vector",
// o "MetafileRenderingMode.VectorWithFallback", representaremos todos los metarchivos como gráficos vectoriales.
// Si establecemos la propiedad "RenderingMode" en "MetafileRenderingMode.Bitmap", representaremos todos los metarchivos como mapas de bits.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Ver también

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../imagesaveoptions/)
* asamblea [Aspose.Words](../../../)


