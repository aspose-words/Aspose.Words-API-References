---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words para .NET
description: Optimice sus imágenes PDF con la propiedad JpegQuality de PdfSaveOptions, que le permite controlar la calidad JPEG para obtener imágenes impactantes del documento.
type: docs
weight: 220
url: /es/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF.

```csharp
public int JpegQuality { get; set; }
```

## Observaciones

El valor predeterminado es 100.

Esta propiedad se utiliza junto con la[`ImageCompression`](../imagecompression/) opción.

Tiene efecto sólo cuando un documento contiene imágenes JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes dentro de un documento al guardarlo en formato PDF. El valor puede variar de 0 a 100, donde 0 significa peor calidad pero máxima compresión y 100 significa mejor calidad pero mínima compresión. Si la calidad es 100 y la imagen de origen es JPEG, significa que no hay compresión: se guardarán los bytes originales.

## Ejemplos

Muestra cómo especificar un tipo de compresión para todas las imágenes de un documento que estamos convirtiendo a PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// Establezca la propiedad "ImageCompression" en "PdfImageCompression.Auto" para utilizar el
// Propiedad "ImageCompression" para controlar la calidad de las imágenes Jpeg que terminan en el PDF de salida.
// Establezca la propiedad "ImageCompression" en "PdfImageCompression.Jpeg" para utilizar el
// Propiedad "ImageCompression" para controlar la calidad de todas las imágenes que terminan en el PDF de salida.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Establezca la propiedad "JpegQuality" en "10" para fortalecer la compresión a costa de la calidad de la imagen.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
