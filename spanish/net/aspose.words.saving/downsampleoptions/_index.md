---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.DownsampleOptions para personalizar fácilmente el muestreo reducido de imágenes para optimizar el rendimiento y la calidad del documento.
type: docs
weight: 5720
url: /es/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Permite especificar opciones de reducción de resolución.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) Artículo de documentación.

```csharp
public class DownsampleOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Especifica si las imágenes deben reducirse de resolución. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Especifica la resolución en píxeles por pulgada a la que se deben reducir las muestras de las imágenes. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Especifica la resolución del umbral en píxeles por pulgada. Si la resolución de una imagen en el documento es menor que el valor del umbral, no se aplicará el algoritmo de reducción de tamaño. Un valor de 0 significa que no se utiliza la comprobación del umbral y se reducen las muestras de todas las imágenes que se pueden reducir de tamaño. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
