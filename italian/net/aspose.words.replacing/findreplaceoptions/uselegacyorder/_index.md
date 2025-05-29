---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words per .NET
description: Scopri la proprietà UseLegacyOrder in FindReplaceOptions. Abilita le ricerche di testo sequenziali per una maggiore precisione. Il valore predefinito è false. Ottimizza l'elaborazione del testo!
type: docs
weight: 180
url: /it/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

Vero indica che una ricerca di testo viene eseguita in sequenza dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è`falso` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Esempi

Mostra come modificare l'ordine di ricerca dei nodi quando si esegue un'operazione di ricerca e sostituzione di testo.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inseriamo tre esecuzioni che possiamo ricercare utilizzando uno schema regex.
    // Inserisci una di queste esecuzioni all'interno di una casella di testo.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Assegna un callback personalizzato alla proprietà "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Se impostiamo la proprietà "UseLegacyOrder" su "true",
    // l'operazione di ricerca e sostituzione esaminerà tutte le esecuzioni al di fuori di una casella di testo
    // prima di passare in rassegna quelli all'interno di una casella di testo.
    // Se impostiamo la proprietà "UseLegacyOrder" su "false",
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
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
