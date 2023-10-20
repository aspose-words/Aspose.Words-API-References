---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words per .NET
description: Aspose.Words.WarningType enum. Specifica il tipo di avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento in C#.
type: docs
weight: 6660
url: /it/net/aspose.words/warningtype/
---
## WarningType enumeration

Specifica il tipo di avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento.

```csharp
[Flags]
public enum WarningType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| DataLossCategory | `FF` | Parte del testo/carattere/immagine o altri dati mancheranno dall'albero del documento dopo il caricamento, o dal documento creato dopo il salvataggio. |
| DataLoss | `1` | Perdita di dati generica, nessun codice specifico. |
| MajorFormattingLossCategory | `FF00` | Il documento risultante o una posizione particolare in esso potrebbe apparire sostanzialmente diverso rispetto al documento originale. |
| MajorFormattingLoss | `100` | Grossa perdita di formattazione generica, nessun codice specifico. |
| MinorFormattingLossCategory | `FF0000` | Il documento risultante o una posizione particolare in esso potrebbe apparire leggermente diversa rispetto al documento originale. |
| MinorFormattingLoss | `10000` | Lieve perdita di formattazione generica, nessun codice specifico. |
| FontSubstitution | `20000` | Il carattere è stato sostituito. |
| FontEmbedding | `40000` | Perdita delle informazioni sui caratteri incorporati durante il salvataggio del documento. |
| UnexpectedContentCategory | `F000000` | Alcuni contenuti del documento di origine non possono essere riconosciuti (ovvero non sono supportati), ciò potrebbe o meno causare problemi o provocare perdite di dati/formattazione. |
| UnexpectedContent | `1000000` | Contenuto generico imprevisto, nessun codice specifico. |
| Hint | `10000000` | Avverte di un potenziale problema o suggerisce un miglioramento. |

## Esempi

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
