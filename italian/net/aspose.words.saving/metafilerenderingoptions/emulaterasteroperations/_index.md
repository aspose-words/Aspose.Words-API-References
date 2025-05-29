---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words per .NET
description: Scopri la proprietà EmulateRasterOperations di MetafileRenderingOptions per controllare l'emulazione delle operazioni raster, migliorando in modo efficace le tue capacità di rendering.
type: docs
weight: 30
url: /it/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Ottiene o imposta un valore che determina se le operazioni raster devono essere emulate o meno.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Osservazioni

Nei metafile potrebbero essere utilizzate operazioni raster specifiche. Non è possibile renderizzarle direttamente in grafica vettoriale. L'emulazione delle operazioni raster richiede una rasterizzazione parziale della grafica vettoriale risultante, che potrebbe influire sulle prestazioni di rendering dei metafile.

Quando questo valore è impostato su`VERO`Aspose.Words emula le operazioni raster. L'output risultante potrebbe essere parzialmente rasterizzato e le prestazioni potrebbero essere più lente.

Quando questo valore è impostato su`falso`Aspose.Words non emula le operazioni raster. Quando Aspose.Words incontra un'operazione raster in un metafile, esegue il rendering del metafile in una bitmap utilizzando il sistema operativo .

Questa opzione viene utilizzata solo quando il metafile viene renderizzato come grafica vettoriale.

Il valore predefinito è`VERO`.

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

* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
