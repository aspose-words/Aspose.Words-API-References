---
title: Enum WarningType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.WarningType enum. Specifica il tipo di avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento.
type: docs
weight: 6350
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
| DataLossCategory | `FF` | Alcuni dati di testo/carattere/immagine o altri dati mancheranno dall'albero del documento dopo il caricamento, o dal documento creato dopo il salvataggio. |
| DataLoss | `1` | Perdita di dati generica, nessun codice specifico. |
| MajorFormattingLossCategory | `FF00` | Il documento risultante o una posizione particolare al suo interno potrebbe avere un aspetto sostanzialmente diverso rispetto al documento originale. |
| MajorFormattingLoss | `100` | Perdita di formattazione maggiore generica, nessun codice specifico. |
| MinorFormattingLossCategory | `FF0000` | Il documento risultante o una posizione particolare al suo interno potrebbe avere un aspetto leggermente diverso rispetto a al documento originale. |
| MinorFormattingLoss | `10000` | Perdita di formattazione secondaria generica, nessun codice specifico. |
| FontSubstitution | `20000` | Il carattere è stato sostituito. |
| FontEmbedding | `40000` | Perdita delle informazioni sui caratteri incorporati durante il salvataggio del documento. |
| UnexpectedContentCategory | `F000000` | Non è stato possibile riconoscere alcuni contenuti nel documento di origine (ovvero non sono supportati), ciò potrebbe causare o meno problemi o causare la perdita di dati/formattazione. |
| UnexpectedContent | `1000000` | Contenuto imprevisto generico, nessun codice specifico. |
| Hint | `10000000` | Segnala un potenziale problema o suggerisce un miglioramento. |

### Esempi

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


