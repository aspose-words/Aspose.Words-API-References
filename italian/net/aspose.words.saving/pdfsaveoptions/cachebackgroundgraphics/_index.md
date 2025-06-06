---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words per .NET
description: Scopri la proprietà CacheBackgroundGraphics di PdfSaveOptions per ottimizzare la memorizzazione nella cache della grafica dei documenti, migliorando così la creazione e le prestazioni dei tuoi PDF.
type: docs
weight: 40
url: /it/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Ottiene o imposta un valore che determina se memorizzare o meno nella cache la grafica posizionata sullo sfondo del documento.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO` e la grafica di sfondo viene scritta nel documento PDF come xObject.

Quando il valore è`falso` la grafica di sfondo non viene memorizzata nella cache.

Alcune forme non sono supportate per la memorizzazione nella cache (forme con campi, segnalibri, HRef).

La grafica di sfondo del documento è composta da varie forme, grafici, immagini posizionate nel piè di pagina o nell'intestazione, nonché dallo sfondo e dal bordo di una pagina.

## Esempi

Mostra come memorizzare nella cache la grafica posizionata sullo sfondo del documento.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
