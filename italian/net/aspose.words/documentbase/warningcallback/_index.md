---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words per .NET
description: Scopri la proprietà WarningCallback di DocumentBase, fondamentale per garantire l'integrità dei dati durante l'elaborazione dei documenti, rilevando potenziali problemi di formattazione.
type: docs
weight: 100
url: /it/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare una perdita di fedeltà dei dati o della formattazione.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Osservazioni

Un documento può generare avvisi in qualsiasi fase della sua esistenza, quindi è importante impostare il callback di avviso il prima possibile per evitare la perdita di avvisi. Ad esempio, proprietà come[`PageCount`](../../document/pagecount/) crea effettivamente il layout del documento che verrà utilizzato in seguito per il rendering e gli avvisi di layout potrebbero andare persi se il callback di avviso viene specificato solo per le chiamate di rendering successive.

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

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
