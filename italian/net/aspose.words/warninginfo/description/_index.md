---
title: WarningInfo.Description
second_title: Aspose.Words per .NET API Reference
description: WarningInfo proprietà. Restituisce la descrizione dellavviso.
type: docs
weight: 10
url: /it/net/aspose.words/warninginfo/description/
---
## WarningInfo.Description property

Restituisce la descrizione dell'avviso.

```csharp
public string Description { get; }
```

### Esempi

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

* class [WarningInfo](../)
* spazio dei nomi [Aspose.Words](../../warninginfo/)
* assemblea [Aspose.Words](../../../)


