---
title: ReplacingArgs.GroupIndex
second_title: Aspose.Words per .NET API Reference
description: ReplacingArgs proprietà. Identifica per indice un gruppo catturato nel fileMatch che va sostituito con ilReplacement stringa.
type: docs
weight: 10
url: /it/net/aspose.words.replacing/replacingargs/groupindex/
---
## ReplacingArgs.GroupIndex property

Identifica, per indice, un gruppo catturato nel file[`Match`](../match/) che va sostituito con il[`Replacement`](../replacement/) stringa.

```csharp
public int GroupIndex { get; set; }
```

### Osservazioni

`GroupIndex`ha effetto solo quando[`GroupName`](../groupname/) È`nullo`.

L'impostazione predefinita è zero.

### Esempi

Mostra come applicare un carattere diverso al nuovo contenuto tramite FindReplaceOptions.

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Imposta la proprietà "HighlightColor" su un colore di sfondo che vogliamo applicare al testo risultante dall'operazione.
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

* class [ReplacingArgs](../)
* spazio dei nomi [Aspose.Words.Replacing](../../replacingargs/)
* assemblea [Aspose.Words](../../../)


