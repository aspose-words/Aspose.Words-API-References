---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words per .NET
description: Scopri l'enum FindReplaceDirection di Aspose.Words per una sostituzione efficiente del testo. Ottimizza l'elaborazione dei tuoi documenti con un controllo preciso della direzione.
type: docs
weight: 5340
url: /it/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

Specifica la direzione per le operazioni di sostituzione.

```csharp
public enum FindReplaceDirection
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Forward | `0` | Gli elementi corrispondenti vengono sostituiti dal primo all'ultimo. |
| Backward | `1` | Gli elementi corrispondenti vengono sostituiti dall'ultimo al primo. |

## Esempi

Mostra come determinare la direzione in cui un'operazione di ricerca e sostituzione attraversa il documento.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inseriamo tre esecuzioni che possiamo ricercare utilizzando uno schema regex.
    // Inserisci una di queste esecuzioni all'interno di una casella di testo.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Assegna un callback personalizzato alla proprietà "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Imposta la proprietà "Direction" su "FindReplaceDirection.Backward" per ottenere la funzione di ricerca e sostituzione
    // operazione per iniziare dalla fine dell'intervallo e tornare all'inizio.
    // Imposta la proprietà "Direction" su "FindReplaceDirection.Forward" per ottenere la funzione di ricerca e sostituzione
    // operazione per iniziare dall'inizio dell'intervallo e attraversarlo fino alla fine.
    options.Direction = findReplaceDirection;

    doc.Range.Replace(new Regex(@"Match \d*"), "Replacement", options);

    Assert.AreEqual("Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.", doc.GetText().Trim());

    switch (findReplaceDirection)
    {
        case FindReplaceDirection.Forward:
            Assert.AreEqual(new[] { "Match 1", "Match 2", "Match 3", "Match 4" }, callback.Matches);
            break;
        case FindReplaceDirection.Backward:
            Assert.AreEqual(new[] { "Match 4", "Match 3", "Match 2", "Match 1" }, callback.Matches);
            break;
    }
}

/// <summary>
/// Registra tutte le corrispondenze che si verificano durante un'operazione di ricerca e sostituzione nell'ordine in cui si verificano.
/// </summary>
private class TextReplacementRecorder : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Replacing](../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../)
