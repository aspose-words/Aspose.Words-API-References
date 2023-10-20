---
title: ReplaceAction Enum
linktitle: ReplaceAction
articleTitle: ReplaceAction
second_title: Aspose.Words für .NET
description: Aspose.Words.Replacing.ReplaceAction opsomming. Ermöglicht dem Benutzer festzulegen was mit der aktuellen Übereinstimmung während eines Ersetzungsvorgangs geschieht in C#.
type: docs
weight: 4640
url: /de/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

Ermöglicht dem Benutzer festzulegen, was mit der aktuellen Übereinstimmung während eines Ersetzungsvorgangs geschieht.

```csharp
public enum ReplaceAction
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Replace | `0` | Ersetzt die aktuelle Übereinstimmung. |
| Skip | `1` | Das aktuelle Spiel überspringen. |
| Stop | `2` | Beenden Sie den Ersetzungsvorgang. |

## Beispiele

Zeigt, wie der Inhalt eines gesamten Dokuments als Ersatz für eine Übereinstimmung in einem Suchen-und-Ersetzen-Vorgang eingefügt wird.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
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

        // Ein Dokument nach dem Absatz einfügen, der den übereinstimmenden Text enthält.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Den Absatz mit dem übereinstimmenden Text entfernen.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Fügt alle Knoten eines anderen Dokuments nach einem Absatz oder einer Tabelle ein.
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
                // Den Knoten überspringen, wenn es sich um den letzten leeren Absatz in einem Abschnitt handelt.
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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* namensraum [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Montage [Aspose.Words](../../)
