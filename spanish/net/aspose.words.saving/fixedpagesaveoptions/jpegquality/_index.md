---
title: FixedPageSaveOptions.JpegQuality
second_title: Referencia de API de Aspose.Words para .NET
description: FixedPageSaveOptions propiedad. Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento HTML.
type: docs
weight: 20
url: /es/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento HTML.

```csharp
public int JpegQuality { get; set; }
```

### Observaciones

Solo tiene efecto cuando un documento contiene imágenes JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes dentro de un documento al guardar en formato de página fijo. El valor puede variar de 0 a 100, donde 0 significa peor calidad pero máxima compresión y 100 significa mejor calidad pero mínima compresión.

El valor predeterminado es 95.

### Ejemplos

Muestra cómo configurar la compresión al guardar un documento como JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Establezca la propiedad "JpegQuality" en "10" para usar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más prominentes.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Establezca la propiedad "JpegQuality" en "100" para usar una compresión más débil al procesar el documento.
// Esto mejorará la calidad de la imagen a costa de aumentar el tamaño del archivo.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Ver también

* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* asamblea [Aspose.Words](../../../)


