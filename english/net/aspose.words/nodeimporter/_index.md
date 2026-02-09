---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words for .NET
description: Effortlessly transfer document nodes with Aspose.Words.NodeImporter. Streamline your workflow and enhance document management efficiency today!
type: docs
weight: 4940
url: /net/aspose.words/nodeimporter/
---
## NodeImporter class

Allows to efficiently perform repeated import of nodes from one document to another.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public class NodeImporter
```

## Constructors

| Name | Description |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Initializes a new instance of the `NodeImporter` class. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Initializes a new instance of the `NodeImporter` class. |

## Methods

| Name | Description |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Imports a node from one document into another. |

## Remarks

Aspose.Words provides functionality for easy copying and moving fragments between Microsoft Word documents. This is known as "importing nodes". Before you can insert a fragment from one document into another, you need to "import" it. Importing creates a deep clone of the original node, ready to be inserted into the destination document.

The simplest way to import a node is to use the [`ImportNode`](../documentbase/importnode/) method provided by the [`DocumentBase`](../documentbase/) object.

However, when you need to import nodes from one document to another multiple times, it is better to use the `NodeImporter` class. The `NodeImporter` class allows to minimize the number of styles and lists created in the destination document.

Copying or moving fragments from one Microsoft Word document to another presents a number of technical challenges for Aspose.Words. In a Word document, styles and list formatting are stored centrally, separately from the text of the document. The paragraphs and runs of text merely reference the styles by internal unique identifiers.

The challenges arise from the fact that styles and lists are different in different documents. For example, to copy a paragraph formatted with the Heading 1 style from one document to another, a number of things must be taken into account: decide whether to copy the Heading 1 style from the source document to the destination document, clone the paragraph, update the cloned paragraph so it refers to the correct Heading 1 style in the destination document. If the style had to be copied, all the styles that it references (based on style and next paragraph style) should be analyzed and possibly copied too and so on. Similar issues exist when copying bulleted or numbered paragraphs because Microsoft Word stores list definitions separately from text.

The `NodeImporter` class is like a context, that holds the "translation tables" during the import. It correctly translates between styles and lists in the source and destination documents.

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
