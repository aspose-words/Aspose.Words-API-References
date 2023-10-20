---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words per .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage proprietà. Ottiene o imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alla dimensione su page o la visualizzazione del metafile nella sua dimensione predefinita in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Ottiene o imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alla dimensione su page o la visualizzazione del metafile nella sua dimensione predefinita.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Osservazioni

Quando i metafile vengono visualizzati in MS Word, alcuni elementi grafici potrebbero essere ridimensionati in base alla dimensione effettiva del metafile in pixel. Ciò significa che anche lo zoom potrebbe influire sulla visualizzazione del metafile.

Quando questo valore è impostato su`VERO` Aspose.Words emula il rendering in base alla dimensione del metafile sulla pagina. La dimensione in pixel viene calcolata dalla dimensione del metafile sulla pagina e dal valore specificato[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Quando questo valore è impostato su`falso`, Aspose.Words emula il rendering del metafile riportandolo alla dimensione predefinita in pixel.

Questa opzione viene utilizzata solo quando il metafile viene visualizzato come grafica vettoriale.

Il valore predefinito è`VERO`.

## Esempi

Mostra come visualizzare il metafile in base alla dimensione della pagina.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "EmulateRenderingToSizeOnPage" su "true"
// per emulare il rendering in base alla dimensione del metafile sulla pagina.
// Imposta la proprietà "EmulateRenderingToSizeOnPage" su "false"
// per emulare il rendering del metafile alla dimensione predefinita in pixel.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Guarda anche

* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
