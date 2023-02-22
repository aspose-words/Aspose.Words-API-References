---
title: FindReplaceOptions.ReplacingCallback
second_title: Aspose.Words per .NET API Reference
description: FindReplaceOptions proprietà. Il metodo definito dallutente che viene chiamato prima di ogni occorrenza di sostituzione.
type: docs
weight: 130
url: /it/net/aspose.words.replacing/findreplaceoptions/replacingcallback/
---
## FindReplaceOptions.ReplacingCallback property

Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione.

```csharp
public IReplacingCallback ReplacingCallback { get; set; }
```

### Esempi

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con un'altra stringa, tenendo traccia di tutte queste sostituzioni.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Imposta un callback che tenga traccia di tutte le sostituzioni che il metodo "Replace" effettuerà.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro di ogni sostituzione di testo eseguita da un'operazione di ricerca e sostituzione
/// e annota il valore del testo corrispondente originale.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Mostra come applicare un carattere diverso al nuovo contenuto tramite FindReplaceOptions.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Imposta la proprietà "HighlightColor" su un colore di sfondo che vogliamo applicare al testo risultante dell'operazione.
    options.ApplyFont.HighlightColor = Color.LightGray;

    NumberHexer numberHexer = new NumberHexer();
    options.ReplacingCallback = numberHexer;

    int replacementCount = doc.Range.Replace(new Regex("[0-9]+"), "", options);

    Console.WriteLine(numberHexer.GetLog());

    Assert.AreEqual(4, replacementCount);
    Assert.AreEqual("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
                    "0x7B, 0x1C8, 0x315 and 0x43E3.", doc.GetText().Trim());
    Assert.AreEqual(4, doc.GetChildNodes(NodeType.Run, true).OfType<Run>()
            .Count(r => r.Font.HighlightColor.ToArgb() == Color.LightGray.ToArgb()));
}

/// <summary>
/// Sostituisce le corrispondenze numeriche di ricerca e sostituzione con i loro equivalenti esadecimali.
/// Mantiene un registro di ogni sostituzione.
/// </summary>
private class NumberHexer : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mCurrentReplacementNumber++;

        int number = Convert.ToInt32(args.Match.Value);

        args.Replacement = $"0x{number:X}";

        mLog.AppendLine($"Match #{mCurrentReplacementNumber}");
        mLog.AppendLine($"\tOriginal value:\t{args.Match.Value}");
        mLog.AppendLine($"\tReplacement:\t{args.Replacement}");
        mLog.AppendLine($"\tOffset in parent {args.MatchNode.NodeType} node:\t{args.MatchOffset}");

        mLog.AppendLine(string.IsNullOrEmpty(args.GroupName)
            ? $"\tGroup index:\t{args.GroupIndex}"
            : $"\tGroup name:\t{args.GroupName}");

        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private int mCurrentReplacementNumber;
    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Guarda anche

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../findreplaceoptions/)
* assemblea [Aspose.Words](../../../)


