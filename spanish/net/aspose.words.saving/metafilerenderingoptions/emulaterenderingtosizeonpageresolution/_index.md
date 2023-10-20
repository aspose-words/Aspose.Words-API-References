---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words para .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution propiedad. Obtiene o establece la resolución en píxeles por pulgada para la emulación de la representación de metarchivos al tamaño de la página en C#.
type: docs
weight: 50
url: /es/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Obtiene o establece la resolución en píxeles por pulgada para la emulación de la representación de metarchivos al tamaño de la página.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Observaciones

Esta opción se utiliza sólo cuando[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) se establece en`verdadero`.

El valor predeterminado es 96. Esta es una resolución de pantalla predeterminada. Es decir, la representación del metarchivo emulará la visualización del metarchivo en MS Word con un factor de zoom del 100%.

## Ejemplos

Muestra cómo visualizar el metarchivo según el tamaño de la página.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establece la propiedad "EmulateRenderingToSizeOnPage" en "true"
// para emular la representación según el tamaño del metarchivo en la página.
// Establece la propiedad "EmulateRenderingToSizeOnPage" en "falso"
// para emular la representación del metarchivo a su tamaño predeterminado en píxeles.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Ver también

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
