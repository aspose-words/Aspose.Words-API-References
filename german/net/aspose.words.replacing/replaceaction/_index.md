---
title: ReplaceAction Enum
linktitle: ReplaceAction
articleTitle: ReplaceAction
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.ReplaceAction, um die Übereinstimmungsergebnisse Ihrer Ersetzungsvorgänge zu steuern und so die Effizienz und Präzision der Dokumentbearbeitung zu verbessern.
type: docs
weight: 5370
url: /de/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

Ermöglicht dem Benutzer anzugeben, was während eines Ersetzungsvorgangs mit der aktuellen Übereinstimmung geschieht.

```csharp
public enum ReplaceAction
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Replace | `0` | Ersetzen Sie die aktuelle Übereinstimmung. |
| Skip | `1` | Überspringe das aktuelle Spiel. |
| Stop | `2` | Beenden Sie den Ersetzungsvorgang. |

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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* namensraum [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Montage [Aspose.Words](../../)
