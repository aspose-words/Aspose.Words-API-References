---
title: ReplacingArgs.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: Aspose.Words per .NET
description: Scopri come utilizzare efficacemente la proprietà GroupName per sostituire i gruppi acquisiti nelle tue corrispondenze con stringhe personalizzate. Migliora le tue capacità di manipolazione delle stringhe!
type: docs
weight: 20
url: /it/net/aspose.words.replacing/replacingargs/groupname/
---
## ReplacingArgs.GroupName property

Identifica, per nome, un gruppo catturato nel[`Match`](../match/) che deve essere sostituito con il[`Replacement`](../replacement/) stringa.

```csharp
public string GroupName { get; set; }
```

## Osservazioni

Quando il nome del gruppo è`null` ,[`GroupIndex`](../groupindex/) viene utilizzato per identificare il gruppo.

Il valore predefinito è`null`.

## Esempi

Mostra come applicare un font diverso al nuovo contenuto tramite FindReplaceOptions.

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

    // Imposta la proprietà "HighlightColor" sul colore di sfondo che vogliamo applicare al testo risultante dall'operazione.
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
/// Sostituisce le corrispondenze numeriche tramite ricerca e sostituzione con i loro equivalenti esadecimali.
/// Tiene un registro di ogni sostituzione.
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
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
