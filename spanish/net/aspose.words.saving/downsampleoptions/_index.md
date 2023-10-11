---
title: Class DownsampleOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.DownsampleOptions clase. Permite especificar opciones de reducción de resolución.
type: docs
weight: 4970
url: /es/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Permite especificar opciones de reducción de resolución.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) artículo de documentación.

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
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Especifica si se debe reducir la resolución de las imágenes. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Especifica la resolución en píxeles por pulgada a la que se deben reducir las imágenes. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Especifica el umbral de resolución en píxeles por pulgada. Si la resolución de una imagen en el documento es inferior al valor umbral, no se aplicará el algoritmo de reducción de resolución. Un valor de 0 significa que no se utiliza la verificación del umbral y todas las imágenes que se pueden reducir en tamaño y se reducen la resolución. |

### Ejemplos

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


