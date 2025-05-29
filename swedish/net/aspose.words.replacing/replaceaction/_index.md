---
title: ReplaceAction Enum
linktitle: ReplaceAction
articleTitle: ReplaceAction
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ReplaceAction-enum för att kontrollera matchningsresultat i dina ersättningsåtgärder, vilket förbättrar effektiviteten och precisionen vid dokumentredigering.
type: docs
weight: 5370
url: /sv/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

Låter användaren ange vad som händer med den aktuella matchningen under en ersättningsåtgärd.

```csharp
public enum ReplaceAction
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Replace | `0` | Ersätt den aktuella matchningen. |
| Skip | `1` | Hoppa över den aktuella matchningen. |
| Stop | `2` | Avsluta ersättningsåtgärden. |

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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* namnutrymme [Aspose.Words.Replacing](../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../)
