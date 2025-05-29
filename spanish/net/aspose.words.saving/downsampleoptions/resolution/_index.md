---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words para .NET
description: Optimice la calidad de la imagen con la propiedad Resolución DownsampleOptions, que define los píxeles por pulgada ideales para obtener resultados de reducción de resolución superiores.
type: docs
weight: 30
url: /es/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Especifica la resolución en píxeles por pulgada a la que se deben reducir las muestras de las imágenes.

```csharp
public int Resolution { get; set; }
```

## Observaciones

El valor predeterminado es 220 ppp.

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

* class [DownsampleOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
