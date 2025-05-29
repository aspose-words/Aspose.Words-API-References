---
title: ReplacingArgs.MatchNode
linktitle: MatchNode
articleTitle: MatchNode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ReplaceingArgs MatchNode för att enkelt komma åt noden där din matchning börjar, vilket förbättrar din kodningseffektivitet och noggrannhet.
type: docs
weight: 40
url: /sv/net/aspose.words.replacing/replacingargs/matchnode/
---
## ReplacingArgs.MatchNode property

Hämtar noden som innehåller början av matchningen.

```csharp
public Node MatchNode { get; }
```

## Exempel

Visar hur man infogar ett helt dokuments innehåll som en ersättning för en matchning i en sök-och-ersätt-åtgärd.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
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

        // Infoga ett dokument efter stycket som innehåller den matchande texten.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Ta bort stycket med den matchande texten.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Infogar alla noder i ett annat dokument efter ett stycke eller en tabell.
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
                // Hoppa över noden om det är det sista tomma stycket i ett avsnitt.
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

### Se även

* class [Node](../../../aspose.words/node/)
* class [ReplacingArgs](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
