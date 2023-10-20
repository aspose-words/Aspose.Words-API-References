---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.MetafileRenderingOptions classe. Permette di specificare opzioni aggiuntive di rendering del metafile in C#.
type: docs
weight: 5300
url: /it/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Permette di specificare opzioni aggiuntive di rendering del metafile.

Per saperne di più, visita il[Gestione dei metafile di Windows](https://docs.aspose.com/words/net/handling-windows-metafiles/) articolo di documentazione.

```csharp
public class MetafileRenderingOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei metafile EMF+ Dual. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Ottiene o imposta un valore che determina se le operazioni raster devono essere emulate o meno. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Ottiene o imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alla dimensione su page o la visualizzazione del metafile nella sua dimensione predefinita. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Ottiene o imposta la risoluzione in pixel per pollice per l'emulazione del rendering del metafile sulla dimensione della pagina. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle immagini metafile. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei metafile WMF con metafile EMF incorporati. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster. |

## Esempi

Mostra aggiunto un fallback al rendering bitmap e modificando il tipo di avvisi sui record di metafile non supportati.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Imposta la proprietà "EmulateRasterOperations" su "false" per tornare alla bitmap quando
    // incontra un metafile, che richiederà operazioni raster per il rendering nel PDF di output.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Imposta la proprietà "RenderingMode" su "VectorWithFallback" per provare a eseguire il rendering di ogni metafile utilizzando la grafica vettoriale.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui il metodo converte il documento in .PDF e applica la configurazione
    // nel nostro oggetto MetafileRenderingOptions all'operazione di salvataggio.
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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
