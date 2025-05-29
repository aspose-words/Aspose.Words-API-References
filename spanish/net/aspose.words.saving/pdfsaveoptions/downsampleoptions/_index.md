---
title: PdfSaveOptions.DownsampleOptions
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words para .NET
description: Descubra la propiedad DownsampleOptions de PdfSaveOptions para personalizar la calidad de su PDF y optimizar el tamaño del archivo para obtener un mejor rendimiento y claridad.
type: docs
weight: 110
url: /es/net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Permite especificar opciones de reducción de resolución.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

## Ejemplos

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// De forma predeterminada, Aspose.Words reduce la resolución de todas las imágenes de un documento que guardamos en PDF a 220 ppp.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Establezca la propiedad "Resolución" en "36" para reducir la resolución de todas las imágenes a 36 ppp.
options.DownsampleOptions.Resolution = 36;

// Establezca la propiedad "ResolutionThreshold" para aplicar el submuestreo solo a
// imágenes con una resolución superior a 128 ppp.
options.DownsampleOptions.ResolutionThreshold = 128;

//En esta etapa, solo se reducirá la resolución de las dos primeras imágenes del documento.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Ver también

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
