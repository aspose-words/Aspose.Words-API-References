---
title: NodeImporter
linktitle: NodeImporter
second_title: Aspose.Words for .NET API Reference
description: NodeImporter constructor. Initializes a new instance of the NodeImporter class in C#.
type: docs
weight: 10
url: /net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Initializes a new instance of the [`NodeImporter`](../) class.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | DocumentBase | The source document. |
| dstDoc | DocumentBase | The destination document that will be the owner of imported nodes. |
| importFormatMode | ImportFormatMode | Specifies how to merge style formatting that clashes. |

## Examples

Shows how to insert the contents of one document to a bookmark in another document.

```csharp
[Test]
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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* namespace [Aspose.Words](../../nodeimporter/)
* assembly [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Initializes a new instance of the [`NodeImporter`](../) class.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | DocumentBase | The source document. |
| dstDoc | DocumentBase | The destination document that will be the owner of imported nodes. |
| importFormatMode | ImportFormatMode | Specifies how to merge style formatting that clashes. |
| importFormatOptions | ImportFormatOptions | Specifies various options to format imported node. |

## Examples

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
// to identical styles as Aspose.Words imports them into destination documents.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Shows how to resolve list numbering clashes in source and destination documents.

```csharp
// Open a document with a custom list numbering scheme, and then clone it.
// Since both have the same numbering format, the formats will clash if we import one document into the other.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// When we import the document's clone into the original and then append it,
// then the two lists with the same list format will join.
// If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
// that we append to the original will carry on the numbering of the list we append it to.
// This will effectively merge the two lists into one.
// If we set the "KeepSourceNumbering" flag to "true", then the document clone
// list will preserve its original numbering, making the two lists appear as separate lists. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### See Also

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* namespace [Aspose.Words](../../nodeimporter/)
* assembly [Aspose.Words](../../../)
