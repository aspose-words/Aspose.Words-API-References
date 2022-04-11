---
title: ReplacingArgs
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4310
url: /net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Provides data for a custom replace operation.

```csharp
public class ReplacingArgs
```

## Public Members

| Name | Description |
| --- | --- |
| [GroupIndex](groupindex) { get; set; } | Identifies, by index, a captured group in the [`Match`](./match) that is to be replaced with the [`Replacement`](./replacement) string. |
| [GroupName](groupname) { get; set; } | Identifies, by name, a captured group in the [`Match`](./match) that is to be replaced with the [`Replacement`](./replacement) string. |
| [Match](match) { get; } | The Match resulting from a single regular expression match during a Replace. |
| [MatchNode](matchnode) { get; } | Gets the node that contains the beginning of the match. |
| [MatchOffset](matchoffset) { get; } | Gets the zero-based starting position of the match from the start of the node that contains the beginning of the match. |
| [Replacement](replacement) { get; set; } | Gets or sets the replacement string. |

### Examples

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

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
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

Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Insert a document after the paragraph containing the matched text.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Remove the paragraph with the matched text.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Inserts all the nodes of another document after a paragraph or table.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Skip the node if it is the last empty paragraph in a section.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### See Also

* interface [IReplacingCallback](../ireplacingcallback)
* class [Range](../../aspose.words/range)
* method [Replace](../../aspose.words/range/replace)
* namespace [Aspose.Words.Replacing](../../aspose.words.replacing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
