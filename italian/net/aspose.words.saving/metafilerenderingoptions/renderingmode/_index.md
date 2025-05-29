---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà RenderingMode di MetafileRenderingOptions per controllare il modo in cui vengono renderizzate le immagini metafile, migliorando così la qualità e le prestazioni della tua grafica.
type: docs
weight: 60
url: /it/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Ottiene o imposta un valore che determina come devono essere renderizzate le immagini metafile.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## Osservazioni

Il valore predefinito dipende dal formato di salvataggio. Per le immagini èBitmap . Per altri formati èVectorWithFallback.

## Esempi

Mostra l'aggiunta di un fallback al rendering bitmap e la modifica del tipo di avviso sui record di metafile non supportati.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Imposta la proprietà "EmulateRasterOperations" su "false" per tornare alla bitmap quando
    // incontra un metafile che richiederà operazioni raster per essere renderizzato nel PDF di output.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Impostare la proprietà "RenderingMode" su "VectorWithFallback" per provare a eseguire il rendering di ogni metafile utilizzando la grafica vettoriale.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui quel metodo converte il documento in .PDF e applica la configurazione
    // nel nostro oggetto MetafileRenderingOptions per l'operazione di salvataggio.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Stampa e raccoglie gli avvisi relativi alla perdita di formattazione che si verificano durante il salvataggio di un documento.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### Guarda anche

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
