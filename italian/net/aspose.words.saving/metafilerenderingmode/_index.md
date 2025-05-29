---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.Saving.MetafileRenderingMode migliora il rendering dei metafile WMF ed EMF per ottenere la migliore qualità e prestazioni dei documenti.
type: docs
weight: 6070
url: /it/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Specifica come Aspose.Words dovrebbe eseguire il rendering dei metafile WMF ed EMF.

```csharp
public enum MetafileRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words tenta di eseguire il rendering di un metafile come grafica vettoriale. Se Aspose.Words non riesce a eseguire correttamente il rendering di alcuni dei record del metafile in grafica vettoriale, Aspose.Words esegue il rendering di questo metafile in una bitmap. |
| Vector | `1` | Aspose.Words esegue il rendering di un metafile come grafica vettoriale. |
| Bitmap | `2` | Aspose.Words richiama GDI+ per trasformare un metafile in un bitmap e quindi salva il bitmap nel documento di output. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
