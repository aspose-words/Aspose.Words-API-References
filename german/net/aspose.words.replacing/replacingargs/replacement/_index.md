---
title: ReplacingArgs.Replacement
second_title: Aspose.Words für .NET-API-Referenz
description: ReplacingArgs eigendom. Ruft die Ersatzzeichenfolge ab oder legt sie fest.
type: docs
weight: 60
url: /de/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Ruft die Ersatzzeichenfolge ab oder legt sie fest.

```csharp
public string Replacement { get; set; }
```

### Beispiele

Zeigt, wie alle Vorkommen eines regulären Ausdrucksmusters durch eine andere Zeichenfolge ersetzt werden, während alle diese Ersetzungen nachverfolgt werden.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Setzen Sie einen Rückruf, der alle Ersetzungen verfolgt, die die "Replace"-Methode vornimmt.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Verwaltet ein Protokoll über jede Textersetzung, die durch eine Suchen-und-Ersetzen-Operation durchgeführt wird
/// und notiert den Wert des ursprünglichen übereinstimmenden Textes.
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

### Siehe auch

* class [ReplacingArgs](../)
* namensraum [Aspose.Words.Replacing](../../replacingargs/)
* Montage [Aspose.Words](../../../)


