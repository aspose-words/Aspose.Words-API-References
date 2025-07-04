---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words for .NET
description: Effortlessly transfer nodes between documents with NodeImporter's ImportNode method. Enhance your workflow and streamline data integration today!
type: docs
weight: 20
url: /net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Imports a node from one document into another.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | Node | The node to import. |
| isImportChildren | Boolean | `true` to import all child nodes recursively; otherwise, `false`. |

### Return Value

The cloned, imported node. The node belongs to the destination document, but has no parent.

## Remarks

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [`InsertBefore`](../../compositenode/insertbefore/) or [`InsertAfter`](../../compositenode/insertafter/).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

## Examples

Shows how to insert the contents of one document to a bookmark in another document.

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

    Assert.That(doc.GetText().Trim(), Is.EqualTo("We will insert a document here: " +
                    "\rHello world!"));
}

/// <summary>
/// Inserts the contents of a document after the specified node.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Loop through all block-level nodes in the section's body,
        // then clone and insert every node that is not the last empty paragraph of a section.
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

### See Also

* class [Node](../../node/)
* class [NodeImporter](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
