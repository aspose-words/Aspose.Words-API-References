---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words para .NET
description: Ajuste la propiedad JpegQuality en ImageSaveOptions para optimizar la calidad de la imagen JPEG y obtener imágenes impactantes y un mejor rendimiento. ¡Perfecto para desarrolladores!
type: docs
weight: 80
url: /es/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Obtiene o establece un valor que determina la calidad de las imágenes JPEG generadas.

```csharp
public int JpegQuality { get; set; }
```

## Observaciones

Tiene efecto sólo al guardar en JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes generadas al guardar en formato JPEG. El valor puede variar de 0 a 100, donde 0 significa peor calidad pero máxima compresión y 100 significa mejor calidad pero mínima compresión.

El valor predeterminado es 95.

## Ejemplos

Muestra cómo configurar la compresión al guardar un documento como JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Establezca la propiedad "JpegQuality" en "10" para utilizar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más prominentes.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Establezca la propiedad "JpegQuality" en "100" para utilizar una compresión más débil al renderizar el documento.
// Esto mejorará la calidad de la imagen a costa de un mayor tamaño de archivo.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
