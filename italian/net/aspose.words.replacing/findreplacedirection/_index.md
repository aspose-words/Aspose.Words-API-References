---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words per .NET
description: Aspose.Words.Replacing.FindReplaceDirection enum. Specifica la direzione per le operazioni di sostituzione in C#.
type: docs
weight: 4610
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

Mostra come determinare in quale direzione un'operazione di ricerca e sostituzione attraversa il documento.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci tre esecuzioni che possiamo cercare utilizzando un modello regex.
    // Posiziona una di queste esecuzioni all'interno di una casella di testo.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Assegna una richiamata personalizzata alla proprietà "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Imposta la proprietà "Direction" su "FindReplaceDirection.Backward" per ottenere la funzione di ricerca e sostituzione
    // operazione per iniziare dalla fine dell'intervallo e tornare all'inizio.
    // Imposta la proprietà "Direction" su "FindReplaceDirection.Backward" per ottenere la funzione di ricerca e sostituzione
    // operazione per iniziare dall'inizio dell'intervallo e spostarsi fino alla fine.
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
/// Registra tutte le corrispondenze che si verificano durante un'operazione di ricerca e sostituzione nell'ordine in cui hanno luogo.
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
