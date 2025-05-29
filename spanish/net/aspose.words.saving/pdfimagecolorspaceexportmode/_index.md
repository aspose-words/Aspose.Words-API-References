---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words PdfImageColorSpaceExportMode para optimizar la selección de color de imagen en sus documentos PDF para obtener imágenes sorprendentes.
type: docs
weight: 6270
url: /es/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF.

```csharp
public enum PdfImageColorSpaceExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | `0` | Aspose.Words selecciona automáticamente el espacio de color más apropiado para cada imagen. |
| SimpleCmyk | `1` | Aspose.Words convierte imágenes RGB al espacio de color CMYK mediante una fórmula sencilla. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
