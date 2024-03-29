---
title: DownsampleOptions.DownsampleImages
linktitle: DownsampleImages
articleTitle: DownsampleImages
second_title: Aspose.Words para .NET
description: DownsampleOptions DownsampleImages propiedad. Especifica si se debe reducir la resolución de las imágenes en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/downsampleoptions/downsampleimages/
---
## DownsampleOptions.DownsampleImages property

Especifica si se debe reducir la resolución de las imágenes.

```csharp
public bool DownsampleImages { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` .

## Ejemplos

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// De forma predeterminada, Aspose.Words reduce la resolución de todas las imágenes de un documento que guardamos en PDF a 220 ppp.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Establezca la propiedad "Resolución" en "36" para reducir la resolución de todas las imágenes a 36 ppp.
options.DownsampleOptions.Resolution = 36;

// Establece la propiedad "ResolutionThreshold" para aplicar la reducción de resolución solo a
// imágenes con una resolución superior a 128 ppp.
options.DownsampleOptions.ResolutionThreshold = 128;

// En esta etapa, solo se reducirán la resolución de las dos primeras imágenes del documento.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Ver también

* class [DownsampleOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
