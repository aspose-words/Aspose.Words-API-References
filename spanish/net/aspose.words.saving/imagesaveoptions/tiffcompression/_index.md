---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words para .NET
description: Optimice sus imágenes TIFF con la propiedad TiffCompression ImageSaveOptions, que le permite elegir el mejor método de compresión para obtener resultados de calidad.
type: docs
weight: 180
url: /es/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Obtiene o establece el tipo de compresión que se aplicará al guardar las imágenes generadas en formato TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Observaciones

Tiene efecto sólo al guardar en formato TIFF.

El valor predeterminado esLzw.

## Ejemplos

Muestra cómo seleccionar el esquema de compresión a aplicar a un documento que convertimos en una imagen TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Establezca la propiedad "TiffCompression" en "TiffCompression.None" para no aplicar compresión al guardar,
// lo que puede resultar en un archivo de salida muy grande.
// Establezca la propiedad "TiffCompression" en "TiffCompression.Rle" para aplicar la compresión RLE
// Establezca la propiedad "TiffCompression" en "TiffCompression.Lzw" para aplicar la compresión LZW.
// Establezca la propiedad "TiffCompression" en "TiffCompression.Ccitt3" para aplicar la compresión CCITT3.
// Establezca la propiedad "TiffCompression" en "TiffCompression.Ccitt4" para aplicar la compresión CCITT4.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Ver también

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
