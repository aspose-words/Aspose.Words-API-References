---
title: IReplacingCallback class
linktitle: IReplacingCallback class
articleTitle: IReplacingCallback class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Replacing.IReplacingCallback class. Implement this interface if you want to have your own custom method called during a find and replace operation."
type: docs
weight: 30
url: /nodejs-net/aspose.words.replacing/ireplacingcallback/
---

## IReplacingCallback class

Implement this interface if you want to have your own custom method called during a find and replace operation.


### Methods

| Name | Description |
| --- | --- |
|[ replacing(args)](./replacing/#replacingargs) | A user defined method that is called during a replace operation for each match found just before a replace is made. |

### Examples

Shows how to track the order in which a text replacement operation traverses nodes.

```js
test.each([false,
  true])('Order', (differentFirstPageHeaderFooter) => {
  let doc = new aw.Document(base.myDir + "Header and footer types.docx");

  let firstPageSection = doc.firstSection;

  let logger = new ReplaceLog();
  let options = new aw.Replacing.FindReplaceOptions(logger);

  // Using a different header/footer for the first page will affect the search order.
  firstPageSection.pageSetup.differentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
  doc.range.replace(new Regex("(header|footer)"), "", options);

  if (differentFirstPageHeaderFooter)
    expect(logger.text.replace("\r", "")).toEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n");
  else
    expect(logger.text.replace("\r", "")).toEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n");
});


  /// <summary>
  /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
  /// in the state it is in before the replacement takes place.
  /// This will display the order in which the text replacement operation traverses nodes.
  /// </summary>
private class ReplaceLog : IReplacingCallback
{
  public ReplaceAction Replacing(ReplacingArgs args)
  {
    mTextBuilder.AppendLine(args.matchNode.getText());
    return aw.Replacing.ReplaceAction.Skip;
  }

  internal string Text => mTextBuilder.toString();

  private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

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

