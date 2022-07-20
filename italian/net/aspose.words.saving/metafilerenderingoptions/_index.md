---
title: MetafileRenderingOptions
second_title: Aspose.Words per .NET API Reference
description: Consente di specificare ulteriori opzioni di rendering del metafile.
type: docs
weight: 5020
url: /it/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Consente di specificare ulteriori opzioni di rendering del metafile.

```csharp
public class MetafileRenderingOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei metafile EMF+ Dual. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations) { get; set; } | Ottiene o imposta un valore che determina se le operazioni raster devono essere emulate o meno. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle immagini del metafile. |
| [ScaleWmfFontsToMetafileSize](../../aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize) { get; set; } | Ottiene o imposta un valore che determina se ridimensionare o meno i caratteri nel metafile WMF in base alla dimensione del metafile nella pagina. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei metafile WMF con metafile EMF incorporati. |

### Esempi

Mostra aggiunto un fallback al rendering delle bitmap e alla modifica del tipo di avvisi sui record di metafile non supportati.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Imposta la proprietà "EmulateRasterOperations" su "false" per tornare alla bitmap quando
    // incontra un metafile, che richiederà operazioni raster per il rendering nel PDF di output.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Imposta la proprietà "RenderingMode" su "VectorWithFallback" per provare a eseguire il rendering di ogni metafile utilizzando la grafica vettoriale.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui quel metodo converte il documento in .PDF e applica la configurazione
    // nel nostro oggetto MetafileRenderingOptions all'operazione di salvataggio.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->