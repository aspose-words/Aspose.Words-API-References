---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.WarningType, che categorizza gli avvisi durante il caricamento o il salvataggio dei documenti, migliorando l'esperienza di gestione dei documenti.
type: docs
weight: 7510
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
| DataLossCategory | `FF` | Alcuni testi/caratteri/immagini o altri dati mancheranno nell'albero del documento dopo il caricamento, o nel documento creato dopo il salvataggio. |
| DataLoss | `1` | Perdita di dati generica, nessun codice specifico. |
| MajorFormattingLossCategory | `FF00` | Il documento risultante o una posizione particolare in esso potrebbe apparire sostanzialmente diverso rispetto al documento originale. |
| MajorFormattingLoss | `100` | Perdita di formattazione importante generica, nessun codice specifico. |
| MinorFormattingLossCategory | `FF0000` | Il documento risultante o una posizione particolare in esso potrebbe apparire leggermente diverso rispetto al documento originale. |
| MinorFormattingLoss | `10000` | Perdita di formattazione minore generica, nessun codice specifico. |
| FontSubstitution | `20000` | Il font è stato sostituito. |
| FontEmbedding | `40000` | Perdita di informazioni sui font incorporati durante il salvataggio del documento. |
| UnexpectedContentCategory | `F000000` | Alcuni contenuti nel documento di origine non sono stati riconosciuti (ovvero non sono supportati); ciò potrebbe causare problemi o causare perdite di dati/formattazione. |
| UnexpectedContent | `1000000` | Contenuto generico inaspettato, nessun codice specifico. |
| Hint | `10000000` | Segnala un potenziale problema o suggerisce un miglioramento. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
