---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.WarningInfoCollection, una potente classe per la gestione di oggetti WarningInfo, migliorando l'elaborazione dei documenti e la gestione degli errori.
type: docs
weight: 7490
url: /it/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Rappresenta una raccolta tipizzata di[`WarningInfo`](../warninginfo/) oggetti.

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
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implementa il[`IWarningCallback`](../iwarningcallback/) interfaccia. Aggiunge un avviso a questa raccolta. |

## Osservazioni

È possibile utilizzare questo oggetto di raccolta come la forma più semplice di[`IWarningCallback`](../iwarningcallback/) Implementazione per raccogliere tutti gli avvisi generati da Aspose.Words durante un'operazione di caricamento o salvataggio. Creare un'istanza di questa classe e assegnarla a[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) O[`WarningCallback`](../documentbase/warningcallback/) proprietà.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
