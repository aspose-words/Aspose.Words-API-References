---
title: ReplacingArgs class
linktitle: ReplacingArgs class
articleTitle: ReplacingArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Replacing.ReplacingArgs class. Provides data for a custom replace operation"
type: docs
weight: 60
url: /nodejs-net/aspose.words.replacing/replacingargs/
---

## ReplacingArgs class

Provides data for a custom replace operation.
To learn more, visit the [Find and Replace](https://docs.aspose.com/words/nodejs-net/find-and-replace/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [groupIndex](./groupIndex/) | Identifies, by index, a captured group in the Aspose.Words.Replacing.ReplacingArgs.Match that is to be replaced with the [ReplacingArgs.replacement](./replacement/) string. |
| [groupName](./groupName/) | Identifies, by name, a captured group in the Aspose.Words.Replacing.ReplacingArgs.Match that is to be replaced with the [ReplacingArgs.replacement](./replacement/) string. |
| [replacement](./replacement/) | Gets or sets the replacement string. |

### Examples

Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements.

```js
test.skip('ReplaceWithCallback - TODO: WORDSNODEJS-107 - Add support of IReplacingCallback', () => {
    let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);

    builder.writeln("Our new location in New York City is opening tomorrow. " +
            "Hope to see all our NYC-based customers at the opening!");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    let options = new aw.Replacing.FindReplaceOptions();

    // Set a callback that tracks any replacements that the "Replace" method will make.
    let logger = new TextFindAndReplacementLogger();
    options.replacingCallback = logger;

    doc.range.replace(new Regex("New York City|NYC"), "Washington", options);

    expect(doc.getText().trim()).toEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                            "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!");

    expect(logger.GetLog().trim()).toEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                            "\"NYC\" converted to \"Washington\" 42 characters into a Run node.");
  });

/*
    /// <summary>
    /// Maintains a log of every text replacement done by a find-and-replace operation
    /// and notes the original matched text's value.
    /// </summary>
  private class TextFindAndReplacementLogger : IReplacingCallback
  {
    ReplaceAction aw.Replacing.IReplacingCallback.replacing(ReplacingArgs args)
    {
      mLog.AppendLine(`\"${args.match.value}\" converted to \"${args.replacement}\" ` +
              `${args.matchOffset} characters into a ${args.matchNode.nodeType} node.`);

      args.replacement = `(Old value:\"${args.match.value}\") ${args.replacement}`;
      return aw.Replacing.ReplaceAction.Replace;
    }

    public string GetLog()
    {
      return mLog.toString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
  }
```

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

