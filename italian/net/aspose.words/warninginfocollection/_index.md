---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.WarningInfoCollection classe. Rappresenta una raccolta digitata diWarningInfo oggetti in C#.
type: docs
weight: 6640
url: /it/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Rappresenta una raccolta digitata di[`WarningInfo`](../warninginfo/) oggetti.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Ottiene un elemento all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implementa il[`IWarningCallback`](../iwarningcallback/) interfaccia. Aggiunge un avviso a questa raccolta. |

## Osservazioni

È possibile utilizzare questo oggetto raccolta come la forma più semplice di[`IWarningCallback`](../iwarningcallback/) implementazione per raccogliere tutti gli avvisi generati da Aspose.Words durante un'operazione di caricamento o salvataggio. Crea un'istanza di questa classe e assegnala al file[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) O[`WarningCallback`](../documentbase/warningcallback/) proprietà.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
