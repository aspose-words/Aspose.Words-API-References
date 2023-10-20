---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words para .NET
description: FixedPageSaveOptions JpegQuality propiedad. Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento HTML en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento HTML.

```csharp
public int JpegQuality { get; set; }
```

## Observaciones

Tiene efecto sólo cuando un documento contiene imágenes JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes dentro de un documento al guardarlo en formato de página fija. El valor puede variar de 0 a 100, donde 0 significa peor calidad pero compresión máxima y 100 significa mejor calidad pero compresión mínima.

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

// Establece la propiedad "JpegQuality" en "10" para utilizar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más destacados.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Establece la propiedad "JpegQuality" en "100" para utilizar una compresión más débil al renderizar el documento.
// Esto mejorará la calidad de la imagen a costa de un mayor tamaño de archivo.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Ver también

* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
