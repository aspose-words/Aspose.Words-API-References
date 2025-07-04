---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words for .NET
description: Discover the UseLegacyOrder property in FindReplaceOptions. Enable sequential text searches for better accuracy. Default is false. Optimize your text processing!
type: docs
weight: 180
url: /net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is `false`.

```csharp
public bool UseLegacyOrder { get; set; }
```

## Examples

Shows how to change the searching order of nodes when performing a find-and-replace text operation.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insert three runs which we can search for using a regex pattern.
    // Place one of those runs inside a text box.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    FindReplaceOptions options = new FindReplaceOptions();

    // Assign a custom callback to the "ReplacingCallback" property.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // If we set the "UseLegacyOrder" property to "true", the
    // find-and-replace operation will go through all the runs outside of a text box
    // before going through the ones inside a text box.
    // If we set the "UseLegacyOrder" property to "false", the
    // find-and-replace operation will go over all the runs in a range in sequential order.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.That(callback.Matches, Is.EqualTo(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }));
}

/// <summary>
/// Records the order of all matches that occur during a find-and-replace operation.
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

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
