---
title: FindReplaceOptions.UseLegacyOrder
second_title: Aspose.Words per .NET API Reference
description: FindReplaceOptions proprietà. True indica che una ricerca di testo viene eseguita in sequenza dallalto verso il basso considerando le caselle di testo. Il valore predefinito èfalso .
type: docs
weight: 170
url: /it/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True indica che una ricerca di testo viene eseguita in sequenza dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è`falso` .

```csharp
public bool UseLegacyOrder { get; set; }
```

### Esempi

Mostra come modificare l'ordine di ricerca dei nodi durante l'esecuzione di un'operazione di ricerca e sostituzione del testo.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci tre esecuzioni che possiamo cercare utilizzando un modello regex.
    // Posiziona una di queste esecuzioni all'interno di una casella di testo.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Assegna una richiamata personalizzata alla proprietà "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Se impostiamo la proprietà "UseLegacyOrder" su "true", il
    // l'operazione di ricerca e sostituzione eseguirà tutte le esecuzioni al di fuori di una casella di testo
    // prima di esaminare quelli all'interno di una casella di testo.
    // Se impostiamo la proprietà "UseLegacyOrder" su "false", il
    // l'operazione di ricerca e sostituzione esaminerà tutte le esecuzioni in un intervallo in ordine sequenziale.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Registra l'ordine di tutte le corrispondenze che si verificano durante un'operazione di ricerca e sostituzione.
/// </summary>
private class TextReplacementTracker : IReplacingCallback
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

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../findreplaceoptions/)
* assemblea [Aspose.Words](../../../)


