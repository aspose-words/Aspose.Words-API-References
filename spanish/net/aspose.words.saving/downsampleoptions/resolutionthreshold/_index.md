---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: Aspose.Words para .NET
description: Optimice sus imágenes con la propiedad Umbral de Resolución de Opciones de Reducción de Resolución. Controle la reducción de resolución según la resolución para un mejor rendimiento y calidad.
type: docs
weight: 40
url: /es/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Especifica la resolución del umbral en píxeles por pulgada. Si la resolución de una imagen en el documento es menor que el valor del umbral, no se aplicará el algoritmo de reducción de tamaño. Un valor de 0 significa que no se utiliza la comprobación del umbral y se reducen las muestras de todas las imágenes que se pueden reducir de tamaño.

```csharp
public int ResolutionThreshold { get; set; }
```

## Observaciones

El valor predeterminado es 0.

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
