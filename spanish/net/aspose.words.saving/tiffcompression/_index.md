---
title: Enum TiffCompression
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.TiffCompression enumeración. Especifica qué tipo de compresión aplicar al guardar imágenes de páginas en un archivo TIFF.
type: docs
weight: 5630
url: /es/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Especifica qué tipo de compresión aplicar al guardar imágenes de páginas en un archivo TIFF.

```csharp
public enum TiffCompression
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No especifica compresión. |
| Rle | `1` | Especifica el esquema de compresión RLE. |
| Lzw | `2` | Especifica el esquema de compresión LZW. En Java emulado mediante compresión Deflate (Zip). |
| Ccitt3 | `3` | Especifica el esquema de compresión CCITT3. |
| Ccitt4 | `4` | Especifica el esquema de compresión CCITT4. |

### Ejemplos

Muestra cómo seleccionar el esquema de compresión a aplicar a un documento que convertimos en una imagen TIFF.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
            // para modificar la forma en que ese método convierte el documento en una imagen.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Establece la propiedad "TiffCompression" en "TiffCompression.None" para no aplicar compresión al guardar,
            // lo que puede resultar en un archivo de salida muy grande.
            // Establece la propiedad "TiffCompression" en "TiffCompression.Rle" para aplicar compresión RLE
            // Establece la propiedad "TiffCompression" en "TiffCompression.Lzw" para aplicar compresión LZW.
            // Establece la propiedad "TiffCompression" en "TiffCompression.Ccitt3" para aplicar compresión CCITT3.
            // Establece la propiedad "TiffCompression" en "TiffCompression.Ccitt4" para aplicar compresión CCITT4.
            options.TiffCompression = tiffCompression;

            doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);

            switch (tiffCompression)
            {
                case TiffCompression.None:
                    Assert.That(3000000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Rle:
#if NET5_0_OR_GREATER
                    Assert.That(6000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#else
                    Assert.That(600000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#endif
                    break;
                case TiffCompression.Lzw:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt3:
                    Assert.That(90000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt4:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
            }
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


