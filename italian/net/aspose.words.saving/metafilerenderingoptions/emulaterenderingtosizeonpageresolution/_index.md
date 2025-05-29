---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words per .NET
description: Scopri la proprietà MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution. Controlla la risoluzione del rendering dei metafile per una visualizzazione ottimale della pagina.
type: docs
weight: 50
url: /it/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Ottiene o imposta la risoluzione in pixel per pollice per l'emulazione del rendering dei metafile in base alle dimensioni della pagina.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Osservazioni

Questa opzione viene utilizzata solo quando[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) è impostato su`VERO`.

Il valore predefinito è 96. Questa è la risoluzione di visualizzazione predefinita. Il rendering dei metafile emulerà la visualizzazione del metafile in MS Word con un fattore di zoom del 100%.

## Esempi

Mostra come visualizzare il metafile in base alle dimensioni della pagina.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "EmulateRenderingToSizeOnPage" su "true"
// per emulare il rendering in base alla dimensione del metafile sulla pagina.
// Imposta la proprietà "EmulateRenderingToSizeOnPage" su "false"
// per emulare il rendering del metafile nella sua dimensione predefinita in pixel.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Guarda anche

* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
