---
title: NodeImporter class
linktitle: NodeImporter class
articleTitle: NodeImporter class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.NodeImporter class. Allows to efficiently perform repeated import of nodes from one document to another"
type: docs
weight: 860
url: /nodejs-net/aspose.words/nodeimporter/
---

## NodeImporter class

Allows to efficiently perform repeated import of nodes from one document to another.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

Aspose.Words provides functionality for easy copying and moving fragments
between Microsoft Word documents. This is known as "importing nodes".
Before you can insert a fragment from one document into another, you need to "import" it.
Importing creates a deep clone of the original node, ready to be inserted into the
destination document.

The simplest way to import a node is to use the [DocumentBase.importNode()](../documentbase/importNode/#node_boolean) method
provided by the [DocumentBase](../documentbase/) object.

However, when you need to import nodes from one document to another multiple times,
it is better to use the [NodeImporter](./) class. The [NodeImporter](./)
class allows to minimize the number of styles and lists created in the destination document.

Copying or moving fragments from one Microsoft Word document to another presents a number
of technical challenges for Aspose.Words. In a Word document, styles and list formatting
are stored centrally, separately from the text of the document. The paragraphs
and runs of text merely reference the styles by internal unique identifiers.

The challenges arise from the fact that styles and lists are different in different documents.
For example, to copy a paragraph formatted with the Heading 1 style from one document to another,
a number of things must be taken into account: decide whether to copy the Heading 1 style from
the source document to the destination document, clone the paragraph, update the cloned
paragraph so it refers to the correct Heading 1 style in the destination document.
If the style had to be copied, all the styles that it references (based on style
and next paragraph style) should be analyzed and possibly copied too and so on.
Similar issues exist when copying bulleted or numbered paragraphs because Microsoft Word
stores list definitions separately from text.

The [NodeImporter](./) class is like a context, that holds the "translation tables"
during the import. It correctly translates between styles and lists in the source and
destination documents.




### Constructors
| Name | Description |
| --- | --- |
| [NodeImporter(srcDoc, dstDoc, importFormatMode)](./constructor/#documentbase_documentbase_importformatmode) | Initializes a new instance of the [NodeImporter](./) class. |
| [NodeImporter(srcDoc, dstDoc, importFormatMode, importFormatOptions)](./constructor/#documentbase_documentbase_importformatmode_importformatoptions) | Initializes a new instance of the [NodeImporter](./) class. |

### Methods

| Name | Description |
| --- | --- |
|[ importNode(srcNode, isImportChildren)](./importNode/#node_boolean) | Imports a node from one document into another. |

### Examples

Shows how to insert the contents of one document to a bookmark in another document.

```js
test('InsertAtBookmark', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  builder.startBookmark("InsertionPoint");
  builder.write("We will insert a document here: ");
  builder.endBookmark("InsertionPoint");

  let docToInsert = new aw.Document();
  builder = new aw.DocumentBuilder(docToInsert);

  builder.write("Hello world!");

  docToInsert.save(base.artifactsDir + "NodeImporter.InsertAtMergeField.docx");

  let bookmark = doc.range.bookmarks.at("InsertionPoint");
  insertDocument(bookmark.bookmarkStart.parentNode, docToInsert);

  expect(doc.getText().trim()).toEqual("We will insert a document here: " +
                          "\rHello world!");
});


/// <summary>
/// Inserts the contents of a document after the specified node.
/// </summary>
function insertDocument(insertionDestination, docToInsert)
{
  if (insertionDestination.nodeType == aw.NodeType.Paragraph || insertionDestination.nodeType == aw.NodeType.Table)
  {
    let destinationParent = insertionDestination.parentNode;

    let importer =
      new aw.NodeImporter(docToInsert, insertionDestination.document, aw.ImportFormatMode.KeepSourceFormatting);

      // Loop through all block-level nodes in the section's body,
      // then clone and insert every node that is not the last empty paragraph of a section.
    for (var srcSection of docToInsert.sections.toArray())
      for (let srcNode of srcSection.body)
      {
        if (srcNode.nodeType == aw.NodeType.Paragraph)
        {
          let para = srcNode.asParagraph();
          if (para.isEndOfSection && !para.hasChildNodes)
            continue;
        }

        let newNode = importer.importNode(srcNode, true);

        destinationParent.insertAfter(newNode, insertionDestination);
        insertionDestination = newNode;
      }
  }
  else
  {
    throw new Error("The destination node should be either a paragraph or table.");
  }
}
```

### See Also

* module [Aspose.Words](../)
* class [Document](../document/)
* method [DocumentBase.importNode()](../documentbase/importNode/#node_boolean)

