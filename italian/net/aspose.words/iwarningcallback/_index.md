---
title: IWarningCallback Interface
linktitle: IWarningCallback
articleTitle: IWarningCallback
second_title: Aspose.Words per .NET
description: Implementa l'interfaccia Aspose.Words.IWarningCallback per personalizzare i metodi di acquisizione degli avvisi di fedeltà durante il caricamento e il salvataggio dei documenti. Migliora l'integrità dei documenti!
type: docs
weight: 3660
url: /it/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

Implementa questa interfaccia se vuoi che venga chiamato un metodo personalizzato per catturare gli avvisi di perdita di fedeltà che possono verificarsi durante il caricamento o il salvataggio di un documento.

```csharp
public interface IWarningCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning/)(*[WarningInfo](../warninginfo/)*) | Aspose.Words richiama questo metodo quando riscontra qualche problema durante il caricamento o il salvataggio del documento che potrebbe causare la perdita di formattazione o di fedeltà dei dati. |

## Esempi

Mostra come utilizzare l'interfaccia IWarningCallback per monitorare gli avvisi di sostituzione dei font.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Memorizza la raccolta corrente di sorgenti di font, che sarà la sorgente di font predefinita per ogni documento
    // per il quale non specifichiamo una sorgente font diversa.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // A scopo di test, imposteremo Aspose.Words in modo che cerchi i font solo in una cartella che non esiste.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Durante il rendering del documento, non sarà possibile trovare il font "Times New Roman".
    // Ciò genererà un avviso di sostituzione del font, che verrà rilevato dal nostro callback.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Chiamato ogni volta che si verifica un avviso durante il caricamento/salvataggio.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

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

Mostra come impostare la proprietà per trovare la corrispondenza più vicina per un font mancante tra le sorgenti di font disponibili.

```csharp
public void EnableFontSubstitution()
{
    // Apre un documento contenente testo formattato con un font che non esiste in nessuna delle nostre fonti di font.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Assegna un callback per gestire gli avvisi di sostituzione dei font.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Imposta un nome di font predefinito e abilita la sostituzione dei font.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Dopo la sostituzione del font, è necessario utilizzare le metriche originali.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Se salviamo un documento con un font mancante, riceveremo un avviso di sostituzione del font.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Possiamo anche verificare gli avvisi nella raccolta e cancellarli.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Chiamato ogni volta che si verifica un avviso durante il caricamento/salvataggio.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
