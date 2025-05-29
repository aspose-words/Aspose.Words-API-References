---
title: Paragraph.IsEndOfSection
linktitle: IsEndOfSection
articleTitle: IsEndOfSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Paragraph IsEndOfSection-Eigenschaft und ermitteln Sie, ob ein Absatz der letzte im Haupttext eines Abschnitts ist, um die Dokumentstruktur und -übersichtlichkeit zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

Wahr, wenn dieser Absatz der letzte Absatz in der[`Body`](../../body/) (Haupttextgeschichte) eines[`Section`](../../section/) ; andernfalls false.

```csharp
public bool IsEndOfSection { get; }
```

## Beispiele

Zeigt, wie der Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument eingefügt wird.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Fügt den Inhalt eines Dokuments nach dem angegebenen Knoten ein.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Durchlaufe alle Knoten auf Blockebene im Hauptteil des Abschnitts,
        // dann klonen und fügen Sie jeden Knoten ein, der nicht der letzte leere Absatz eines Abschnitts ist.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
