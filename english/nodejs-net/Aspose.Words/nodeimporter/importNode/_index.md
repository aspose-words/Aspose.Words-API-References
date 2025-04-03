---
title: NodeImporter.importNode method
linktitle: importNode method
articleTitle: importNode method
second_title: Aspose.Words for NodeJs
description: "NodeImporter.importNode method. Imports a node from one document into another."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/nodeimporter/importNode/
---

## importNode(srcNode, isImportChildren) {#node_boolean}

Imports a node from one document into another.




```js
importNode(srcNode: Aspose.Words.NodeisImportChildren: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../node/) | The node to import. |
| isImportChildren | boolean | ``true`` to import all child nodes recursively; otherwise, ``false``. |

### Remarks

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node) or 
[CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned, imported node. The node belongs to the destination document, but has no parent.


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

* module [Aspose.Words](../../)
* class [NodeImporter](../)

