---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Replacing.FindReplaceDirection enum. Specifies direction for replace operations in C#.
type: docs
weight: 4520
url: /net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

Specifies direction for replace operations.

```csharp
public enum FindReplaceDirection
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Forward | `0` | Matched items are replaced from first to last. |
| Backward | `1` | Matched items are replaced from last back to first. |

## Examples

Shows how to determine which direction a find-and-replace operation traverses the document in.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insert three runs which we can search for using a regex pattern.
    // Place one of those runs inside a text box.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    FindReplaceOptions options = new FindReplaceOptions();

    // Assign a custom callback to the "ReplacingCallback" property.
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
    // operation to start from the end of the range, and traverse back to the beginning.
    // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
    // operation to start from the beginning of the range, and traverse to the end.
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
/// Records all matches that occur during a find-and-replace operation in the order that they take place.
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

### See Also

* namespace [Aspose.Words.Replacing](../../aspose.words.replacing/)
* assembly [Aspose.Words](../../)
