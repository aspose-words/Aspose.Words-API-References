---
title: PdfSaveOptions.ImageColorSpaceExportMode
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF.
type: docs
weight: 160
url: /es/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

### Observaciones

El valor predeterminado esAuto .

SiSimpleCmyk se especifica el valor, [`ImageCompression`](../imagecompression/) se ignora la opción y se utiliza la compresión Flate para todas las imágenes del documento.

SimpleCmyk el valor no es compatible cuando se guarda en PDF/A. Auto en su lugar se utilizará el valor.

### Ejemplos

Muestra cómo configurar un espacio de color diferente para las imágenes en un documento a medida que lo exportamos a PDF.

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

// Establezca la propiedad "ImageColorSpaceExportMode" en "PdfImageColorSpaceExportMode.Auto" para que Aspose.Words
// selecciona automáticamente el espacio de color para las imágenes en el documento que convierte a PDF.
// En la mayoría de los casos, el espacio de color será RGB.
// Establecer la propiedad "ImageColorSpaceExportMode" en "PdfImageColorSpaceExportMode.SimpleCmyk"
// para usar el espacio de color CMYK para todas las imágenes en el PDF guardado.
// Aspose.Words también aplicará la compresión Flate a todas las imágenes e ignorará el valor de la propiedad "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Ver también

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


