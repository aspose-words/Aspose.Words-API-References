---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words per .NET API Reference
description: MetafileRenderingOptions proprietà. Ottiene o imposta la risoluzione in pixel per pollice per lemulazione del rendering del metafile sulla dimensione della pagina.
type: docs
weight: 50
url: /it/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Ottiene o imposta la risoluzione in pixel per pollice per l'emulazione del rendering del metafile sulla dimensione della pagina.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

### Osservazioni

Questa opzione viene utilizzata solo quando[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) è impostato per`VERO`.

Il valore predefinito è 96. Questa è una risoluzione dello schermo predefinita. Cioè il rendering del metafile emulerà la visualizzazione di il metafile in MS Word con un fattore di zoom del 100%.

### Esempi

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
* spazio dei nomi [Aspose.Words.Saving](../../metafilerenderingoptions/)
* assemblea [Aspose.Words](../../../)


