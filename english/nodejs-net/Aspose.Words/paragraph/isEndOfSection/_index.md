---
title: Paragraph.isEndOfSection property
linktitle: isEndOfSection property
articleTitle: isEndOfSection property
second_title: Aspose.Words for NodeJs
description: "Paragraph.isEndOfSection property. True if this paragraph is the last paragraph in the [Body](../../body/) (main text story) of a [Section](../../section/); false otherwise."
type: docs
weight: 80
url: /nodejs-net/aspose.words/paragraph/isEndOfSection/
---

## Paragraph.isEndOfSection property

True if this paragraph is the last paragraph in the [Body](../../body/) (main text story) of a [Section](../../section/); false otherwise.



```js
get isEndOfSection(): boolean
```

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
* class [Paragraph](../)

