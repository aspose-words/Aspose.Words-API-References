---
title: DocumentBase.WarningCallback
second_title: Aspose.Words per .NET API Reference
description: DocumentBase proprietà. Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare una perdita di fedeltà dei dati o della formattazione.
type: docs
weight: 90
url: /it/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare una perdita di fedeltà dei dati o della formattazione.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Osservazioni

Il documento può generare avvisi in qualsiasi fase della sua esistenza, quindi è importante impostare il callback degli avvisi il prima possibile per evitare la perdita di avvisi. Ad esempio proprietà come[`PageCount`](../../document/pagecount/) crea effettivamente il layout del documento che viene utilizzato in seguito per il rendering e gli avvisi di layout potrebbero andare persi se warning callback viene specificato solo per le chiamate di rendering in un secondo momento.

### Esempi

Mostra come utilizzare l'interfaccia IWarningCallback per monitorare gli avvisi di sostituzione dei caratteri.

```csharp
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

    // Durante il rendering del documento, non ci sarà spazio per trovare il carattere "Times New Roman".
    // Ciò causerà un avviso di sostituzione del carattere, che il nostro callback rileverà.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

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

Mostra come impostare la proprietà per trovare la corrispondenza più vicina per un carattere mancante dalle fonti di carattere disponibili.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Apri un documento che contiene testo formattato con un font che non esiste in nessuna delle nostre fonti di font.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Assegna una richiamata per la gestione degli avvisi di sostituzione dei caratteri.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Imposta un nome di carattere predefinito e abilita la sostituzione dei caratteri.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

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
* spazio dei nomi [Aspose.Words](../../documentbase/)
* assemblea [Aspose.Words](../../../)


