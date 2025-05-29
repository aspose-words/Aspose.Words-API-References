---
title: IWarningCallback.Warning
linktitle: Warning
articleTitle: Warning
second_title: Aspose.Words per .NET
description: Scopri il metodo IWarningCallback in Aspose.Words. Gestisci senza problemi i problemi di caricamento e salvataggio dei documenti, preservando la formattazione e l'integrità dei dati.
type: docs
weight: 10
url: /it/net/aspose.words/iwarningcallback/warning/
---
## IWarningCallback.Warning method

Aspose.Words richiama questo metodo quando riscontra qualche problema durante il caricamento o il salvataggio del documento che potrebbe causare la perdita di formattazione o di fedeltà dei dati.

```csharp
public void Warning(WarningInfo info)
```

## Esempi

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

* class [WarningInfo](../../warninginfo/)
* interface [IWarningCallback](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
