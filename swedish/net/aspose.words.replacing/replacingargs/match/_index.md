---
title: ReplacingArgs.Match
linktitle: Match
articleTitle: Match
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ReplaceingArgs Match för sömlösa regex-ersättningar. Förbättra din kodningseffektivitet med exakta matchningsresultat!
type: docs
weight: 30
url: /sv/net/aspose.words.replacing/replacingargs/match/
---
## ReplacingArgs.Match property

DenMatch resultatet av en enda matchning av regular -uttrycket under en**Ersätta** .

```csharp
public Match Match { get; }
```

## Anmärkningar

**Match.Index"** hämtar den nollbaserade starting -positionen för matchningen från början av sök- och ersättningsintervallet.

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
