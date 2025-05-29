---
title: ReplacingArgs.MatchNode
linktitle: MatchNode
articleTitle: MatchNode
second_title: Aspose.Words für .NET
description: Entdecken Sie die MatchNode-Eigenschaft von ReplacingArgs, um einfach auf den Knoten zuzugreifen, an dem Ihre Übereinstimmung beginnt, und so Ihre Codierungseffizienz und -genauigkeit zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.replacing/replacingargs/matchnode/
---
## ReplacingArgs.MatchNode property

Ruft den Knoten ab, der den Anfang der Übereinstimmung enthält.

```csharp
public Node MatchNode { get; }
```

## Beispiele

Zeigt, wie der gesamte Inhalt eines Dokuments als Ersatz für eine Übereinstimmung in einem Suchen-und-Ersetzen-Vorgang eingefügt wird.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
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

        // Fügen Sie nach dem Absatz, der den übereinstimmenden Text enthält, ein Dokument ein.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Entfernen Sie den Absatz mit dem übereinstimmenden Text.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Fügt nach einem Absatz oder einer Tabelle alle Knoten eines anderen Dokuments ein.
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
                // Überspringe den Knoten, wenn es sich um den letzten leeren Absatz in einem Abschnitt handelt.
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

### Siehe auch

* class [Node](../../../aspose.words/node/)
* class [ReplacingArgs](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
