---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.TiffCompression para optimizar el almacenamiento de archivos TIFF. Elija fácilmente el mejor tipo de compresión para imágenes de página de alta calidad.
type: docs
weight: 6430
url: /es/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Especifica qué tipo de compresión se aplicará al guardar imágenes de página en un archivo TIFF.

```csharp
public enum TiffCompression
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No especifica compresión. |
| Rle | `1` | Especifica el esquema de compresión RLE. |
| Lzw | `2` | Especifica el esquema de compresión LZW. En Java, emulado por la compresión Deflate (Zip). |
| Ccitt3 | `3` | Especifica el esquema de compresión CCITT3. |
| Ccitt4 | `4` | Especifica el esquema de compresión CCITT4. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
