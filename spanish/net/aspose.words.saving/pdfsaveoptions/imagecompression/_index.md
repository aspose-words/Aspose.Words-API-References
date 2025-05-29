---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words para .NET
description: Optimice su PDF con la propiedad ImageCompression de PdfSaveOptions, que le permite elegir el mejor tipo de compresión para imágenes vibrantes y de alta calidad.
type: docs
weight: 200
url: /es/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Especifica el tipo de compresión que se utilizará para todas las imágenes del documento.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Observaciones

El valor predeterminado esAuto.

UsandoJpeg le permite controlar la calidad de las imágenes en el documento de salida a través de[`JpegQuality`](../jpegquality/) propiedad.

UsandoJpeg Proporciona la velocidad de conversión más rápida en comparación con el rendimiento de otros tipos de compresión, pero en este caso, hay compresión JPEG con pérdida.

UsandoAuto Permite controlar la calidad de Jpeg en el documento de salida a través del[`JpegQuality`](../jpegquality/)propiedad, pero para otros formatos, los datos de píxeles sin procesar se extraen y se guardan con compresión Flate. Este caso es más lento que la conversión a Jpeg, pero sin pérdidas.

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
