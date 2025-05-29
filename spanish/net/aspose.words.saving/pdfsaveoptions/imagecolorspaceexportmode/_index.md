---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad PdfSaveOptions ImageColorSpaceExportMode para optimizar la selección de colores de imagen en sus PDF para lograr una consistencia y calidad visual sorprendentes.
type: docs
weight: 190
url: /es/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## Observaciones

El valor predeterminado esAuto .

SiSimpleCmyk se especifica el valor, [`ImageCompression`](../imagecompression/) La opción se ignora y se utiliza compresión plana para todas las imágenes del documento.

SimpleCmyk El valor no es compatible al guardar en PDF/A. Auto Se utilizará el valor en su lugar.

## Ejemplos

Muestra cómo establecer un espacio de color diferente para las imágenes de un documento cuando lo exportamos a PDF.

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

// Establezca la propiedad "ImageColorSpaceExportMode" en "PdfImageColorSpaceExportMode.Auto" para obtener Aspose.Words
// selecciona automáticamente el espacio de color para las imágenes en el documento que convierte a PDF.
// En la mayoría de los casos, el espacio de color será RGB.
// Establezca la propiedad "ImageColorSpaceExportMode" en "PdfImageColorSpaceExportMode.SimpleCmyk"
// para utilizar el espacio de color CMYK para todas las imágenes en el PDF guardado.
// Aspose.Words también aplicará compresión Flate a todas las imágenes e ignorará el valor de la propiedad "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Ver también

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
