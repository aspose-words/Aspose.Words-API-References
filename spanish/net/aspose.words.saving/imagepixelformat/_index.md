---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.ImagePixelFormat para optimizar los formatos de píxeles en las imágenes de las páginas de sus documentos. ¡Mejore el aspecto visual de sus documentos sin esfuerzo!
type: docs
weight: 5970
url: /es/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Especifica el formato de píxeles para las imágenes generadas de las páginas del documento.

```csharp
public enum ImagePixelFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 bits por píxel, RGB. |
| Format16BppRgb565 | `1` | 16 bits por píxel, RGB. |
| Format16BppArgb1555 | `2` | 16 bits por píxel, ARGB. |
| Format24BppRgb | `3` | 24 bits por píxel, RGB. |
| Format32BppRgb | `4` | 32 bits por píxel, RGB. |
| Format32BppArgb | `5` | 32 bits por píxel, ARGB. |
| Format32BppPArgb | `6` | 32 bits por píxel, ARGB, alfa premultiplicado. |
| Format48BppRgb | `7` | 48 bits por píxel, RGB. |
| Format64BppArgb | `8` | 64 bits por píxel, ARGB. |
| Format64BppPArgb | `9` | 64 bits por píxel, ARGB, alfa premultiplicado. |
| Format1bppIndexed | `10` | 1 bit por píxel, indexado. |

## Ejemplos

Muestra cómo seleccionar una velocidad de bits por píxel con la que convertir un documento en una imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// seleccione un formato de píxel para la imagen que generará la operación de guardado.
//Varias tasas de bits por píxel afectarán la calidad y el tamaño del archivo de la imagen generada.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

//Podemos clonar instancias de ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
