---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words per .NET
description: DocumentBase WarningCallback proprietà. Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione in C#.
type: docs
weight: 90
url: /it/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Osservazioni

Il documento può generare avvisi in qualsiasi fase della sua esistenza, quindi è importante impostare la richiamata degli avvisi il più presto possibile per evitare la perdita di avvisi. Ad esempio, proprietà come[`PageCount`](../../document/pagecount/) crea effettivamente il layout del documento che verrà utilizzato successivamente per il rendering e gli avvisi sul layout potrebbero andare persi se il callback di avviso viene specificato solo per le chiamate di rendering successive.

## Esempi

Mostra come utilizzare l'interfaccia IWarningCallback per monitorare gli avvisi di sostituzione dei caratteri.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Memorizza la raccolta corrente di fonti di carattere, che sarà la fonte di carattere predefinita per ogni documento
    // per il quale non specifichiamo una fonte di carattere diversa.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // A scopo di test, imposteremo Aspose.Words per cercare i caratteri solo in una cartella che non esiste.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Durante il rendering del documento, non sarà possibile trovare il carattere "Times New Roman".
    // Ciò causerà un avviso di sostituzione del carattere, che il nostro callback rileverà.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.", StringComparison.Ordinal));
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

Mostra come impostare la proprietà per trovare la corrispondenza più vicina per un carattere mancante tra le origini dei caratteri disponibili.

```csharp
public void EnableFontSubstitution()
{
    // Apre un documento che contiene testo formattato con un carattere che non esiste in nessuna delle nostre fonti di caratteri.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Assegna una richiamata per gestire gli avvisi di sostituzione dei caratteri.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Imposta un nome di carattere predefinito e abilita la sostituzione del carattere.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Le metriche dei caratteri originali devono essere utilizzate dopo la sostituzione dei caratteri.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Riceveremo un avviso di sostituzione del carattere se salviamo un documento con un carattere mancante.
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

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
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
