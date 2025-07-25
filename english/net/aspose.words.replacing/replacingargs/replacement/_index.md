---
title: ReplacingArgs.Replacement
linktitle: Replacement
articleTitle: Replacement
second_title: Aspose.Words for .NET
description: Discover the ReplacingArgs Replacement property to easily manage and customize your replacement strings for enhanced coding efficiency.
type: docs
weight: 70
url: /net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Gets or sets the replacement string.

```csharp
public string Replacement { get; set; }
```

## Examples

Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    FindReplaceOptions options = new FindReplaceOptions();

    // Set a callback that tracks any replacements that the "Replace" method will make.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.That(doc.GetText().Trim(), Is.EqualTo("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!"));

    Assert.That(logger.GetLog().Trim(), Is.EqualTo("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node."));
}

/// <summary>
/// Maintains a log of every text replacement done by a find-and-replace operation
/// and notes the original matched text's value.
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

### See Also

* class [ReplacingArgs](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
