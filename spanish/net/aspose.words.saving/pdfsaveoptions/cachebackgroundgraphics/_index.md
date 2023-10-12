---
title: PdfSaveOptions.CacheBackgroundGraphics
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece un valor que determina si se deben almacenar en caché los gráficos colocados en el fondo del documento.
type: docs
weight: 30
url: /es/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Obtiene o establece un valor que determina si se deben almacenar en caché los gráficos colocados en el fondo del documento.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

### Observaciones

El valor predeterminado es`verdadero` y los gráficos de fondo se escriben en el documento PDF como un xObject.

Cuando el valor es`FALSO` los gráficos de fondo no se almacenan en caché.

Algunas formas no son compatibles con el almacenamiento en caché (formas con campos, marcadores, HRefs).

El gráfico de fondo del documento consta de varias formas, cuadros, imágenes colocadas en el pie de página o encabezado, , así como el fondo y el borde de una página.

### Ejemplos

Muestra cómo almacenar en caché los gráficos colocados en el fondo del documento.

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
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


