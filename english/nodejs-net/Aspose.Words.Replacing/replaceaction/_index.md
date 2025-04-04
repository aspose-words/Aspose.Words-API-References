---
title: ReplaceAction enumeration
linktitle: ReplaceAction enumeration
articleTitle: ReplaceAction enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Replacing.ReplaceAction enumeration. Allows the user to specify what happens to the current match during a replace operation."
type: docs
weight: 40
url: /nodejs-net/aspose.words.replacing/replaceaction/
---

## ReplaceAction enumeration

Allows the user to specify what happens to the current match during a replace operation.


### Members

| Name | Description |
| --- | --- |
| Replace | Replace the current match. |
| Skip | Skip the current match. |
| Stop | Terminate the replace operation. |

### Examples

Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation.

```js
test.skip('InsertDocumentAtReplace - TODO: WORDSNODEJS-106 - Add support of regex to doc.range.replace', () => {
    let mainDoc = new aw.Document(base.myDir + "Document insertion destination.docx");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    let options = new aw.Replacing.FindReplaceOptions();
    options.replacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.range.replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.save(base.artifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

  });

/*
  private class InsertDocumentAtReplaceHandler : IReplacingCallback
  {
    ReplaceAction aw.Replacing.IReplacingCallback.replacing(ReplacingArgs args)
    {
      let subDoc = new aw.Document(base.myDir + "Document.docx");

        // Insert a document after the paragraph containing the matched text.
      let para = (Paragraph)args.matchNode.parentNode;
      InsertDocument(para, subDoc);

        // Remove the paragraph with the matched text.
      para.remove();

      return aw.Replacing.ReplaceAction.Skip;
    }
  }

    /// <summary>
    /// Inserts all the nodes of another document after a paragraph or table.
    /// </summary>
  private static void InsertDocument(Node insertionDestination, Document docToInsert)
  {
    if (insertionDestination.nodeType == aw.NodeType.Paragraph || insertionDestination.nodeType == aw.NodeType.Table)
    {
      let dstStory = insertionDestination.parentNode;

      let importer =
        new aw.NodeImporter(docToInsert, insertionDestination.document, aw.ImportFormatMode.KeepSourceFormatting);

      foreach (Section srcSection in docToInsert.sections.OfType<Section>())
        for (let srcNode of srcSection.body)
        {
            // Skip the node if it is the last empty paragraph in a section.
          if (srcNode.nodeType == aw.NodeType.Paragraph)
          {
            let para = (Paragraph)srcNode;
            if (para.isEndOfSection && !para.hasChildNodes)
              continue;
          }

          let newNode = importer.importNode(srcNode, true);

          dstStory.insertAfter(newNode, insertionDestination);
          insertionDestination = newNode;
        }
    }
    else
    {
      throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
  }
```

### See Also

* module [Aspose.Words.Replacing](../)
* class [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Range.replace()](../../aspose.words/range/replace/#string_string_findreplaceoptions)

