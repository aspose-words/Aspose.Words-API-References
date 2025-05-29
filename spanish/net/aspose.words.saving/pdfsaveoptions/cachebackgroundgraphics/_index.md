---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words para .NET
description: Descubra la propiedad PdfSaveOptions CacheBackgroundGraphics para optimizar el almacenamiento en caché de gráficos de documentos, mejorando así la creación y el rendimiento de sus PDF.
type: docs
weight: 40
url: /es/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Obtiene o establece un valor que determina si se deben almacenar o no en caché los gráficos colocados en el fondo del documento.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` y los gráficos de fondo se escriben en el documento PDF como un xObject.

Cuando el valor es`FALSO` Los gráficos de fondo no se almacenan en caché.

Algunas formas no son compatibles con el almacenamiento en caché (formas con campos, marcadores, HRefs).

El fondo gráfico del documento son varias formas, gráficos e imágenes colocadas en el pie de página o el encabezado, así como en el fondo y el borde de una página.

## Ejemplos

Muestra cómo almacenar en caché gráficos colocados en el fondo del documento.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
