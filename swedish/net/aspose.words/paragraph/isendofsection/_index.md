---
title: Paragraph.IsEndOfSection
second_title: Aspose.Words för .NET API Referens
description: Paragraph fast egendom. Sant om detta stycke är det sista stycket iBody huvudtextberättelse av enSection  falskt annars.
type: docs
weight: 80
url: /sv/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

Sant om detta stycke är det sista stycket i[`Body`](../../body/) (huvudtextberättelse) av en[`Section`](../../section/) ; falskt annars.

```csharp
public bool IsEndOfSection { get; }
```

### Exempel

Visar hur man infogar innehållet i ett dokument till ett bokmärke i ett annat dokument.

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
/// Infogar innehållet i ett dokument efter den angivna noden.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Slinga igenom alla noder på blocknivå i sektionens kropp,
        // klona sedan och infoga varje nod som inte är det sista tomma stycket i ett avsnitt.
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

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


