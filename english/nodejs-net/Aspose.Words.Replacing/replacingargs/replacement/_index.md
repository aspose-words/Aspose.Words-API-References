---
title: ReplacingArgs.replacement property
linktitle: replacement property
articleTitle: replacement property
second_title: Aspose.Words for Node.js
description: "ReplacingArgs.replacement property. Gets or sets the replacement string."
type: docs
weight: 30
url: /nodejs-net/aspose.words.replacing/replacingargs/replacement/
---

## ReplacingArgs.replacement property

Gets or sets the replacement string.


```js
get replacement(): string
```

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

### See Also

* module [Aspose.Words.Replacing](../../)
* class [ReplacingArgs](../)

