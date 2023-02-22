---
title: Enum MetafileRenderingMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.MetafileRenderingMode enum. Specifica come Aspose.Words deve eseguire il rendering dei metafile WMF ed EMF.
type: docs
weight: 5010
url: /it/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Specifica come Aspose.Words deve eseguire il rendering dei metafile WMF ed EMF.

```csharp
public enum MetafileRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words tenta di eseguire il rendering di un metafile come grafica vettoriale. Se Aspose.Words non può eseguire correttamente il rendering di alcuni dei record del metafile in grafica vettoriale, Aspose.Words esegue il rendering di questo metafile in una bitmap. |
| Vector | `1` | Aspose.Words esegue il rendering di un metafile come grafica vettoriale. |
| Bitmap | `2` | Aspose.Words richiama GDI+ per eseguire il rendering di un metafile in una bitmap e quindi salva la bitmap nel documento di output. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


