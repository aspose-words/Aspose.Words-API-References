---
title: ReplacingArgs.GroupIndex
linktitle: GroupIndex
articleTitle: GroupIndex
second_title: Aspose.Words för .NET
description: Lär dig hur du använder GroupIndex-egenskapen i ReplaceingArgs för att enkelt identifiera och ersätta insamlade grupper i matchningar med dina anpassade strängar.
type: docs
weight: 10
url: /sv/net/aspose.words.replacing/replacingargs/groupindex/
---
## ReplacingArgs.GroupIndex property

Identifierar, med hjälp av index, en fångad grupp i[`Match`](../match/) som ska ersättas med[`Replacement`](../replacement/) sträng.

```csharp
public int GroupIndex { get; set; }
```

## Anmärkningar

`GroupIndex` har effekt endast när[`GroupName`](../groupname/) är`null`.

Standardvärdet är noll.

## Exempel

Visar hur man använder ett annat teckensnitt på nytt innehåll via FindReplaceOptions.

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();

    // Ställ in egenskapen "HighlightColor" till en bakgrundsfärg som vi vill använda på operationens resulterande text.
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
/// Ersätter numeriska sök-och-ersätt-träffar med deras hexadecimala motsvarigheter.
/// För en logg över varje byte.
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

### Se även

* class [ReplacingArgs](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
