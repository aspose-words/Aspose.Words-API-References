---
title: PdfSaveOptions.JpegQuality
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF.
type: docs
weight: 220
url: /es/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF.

```csharp
public int JpegQuality { get; set; }
```

### Observaciones

El valor predeterminado es 100.

Esta propiedad se utiliza junto con la[`ImageCompression`](../imagecompression/) opción.

Tiene efecto sólo cuando un documento contiene imágenes JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes dentro de un documento al guardarlo en formato PDF. El valor puede variar de 0 a 100, donde 0 significa peor calidad pero compresión máxima y 100 significa mejor calidad pero compresión mínima. Si es calidad es 100 y la imagen de origen es JPEG, significa que no hay compresión; se guardarán los bytes originales.

### Ejemplos

Muestra cómo especificar un tipo de compresión para todas las imágenes de un documento que estamos convirtiendo a PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Establece la propiedad "ImageCompression" en "PdfImageCompression.Auto" para usar el
// Propiedad "ImageCompression" para controlar la calidad de las imágenes Jpeg que terminan en el PDF de salida.
// Establece la propiedad "ImageCompression" en "PdfImageCompression.Jpeg" para usar el
// Propiedad "ImageCompression" para controlar la calidad de todas las imágenes que terminan en el PDF de salida.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Establezca la propiedad "JpegQuality" en "10" para fortalecer la compresión a costa de la calidad de la imagen.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


