---
title: FindReplaceOptions.useLegacyOrder property
linktitle: useLegacyOrder property
articleTitle: useLegacyOrder property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.useLegacyOrder property. True indicates that a text search is performed sequentially from top to bottom considering the text boxes"
type: docs
weight: 180
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/useLegacyOrder/
---

## FindReplaceOptions.useLegacyOrder property

True indicates that a text search is performed sequentially from top to bottom considering the text boxes.
Default value is ``False``.



```js
get useLegacyOrder(): boolean
```

### Examples

Shows how to change the searching order of nodes when performing a find-and-replace text operation.

```js
test.skip.each([true,
    false])('UseLegacyOrder - TODO: WORDSNODEJS-106 - Add support of regex to doc.range.replace', (useLegacyOrder) => {
    let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);

    // Insert three runs which we can search for using a regex pattern.
    // Place one of those runs inside a text box.
    builder.writeln("[tag 1]");
    let textBox = builder.insertShape(aw.Drawing.ShapeType.TextBox, 100, 50);
    builder.writeln("[tag 2]");
    builder.moveTo(textBox.firstParagraph);
    builder.write("[tag 3]");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    let options = new aw.Replacing.FindReplaceOptions();

    // Assign a custom callback to the "ReplacingCallback" property.
    let callback = new TextReplacementTracker();
    options.replacingCallback = callback;

    // If we set the "UseLegacyOrder" property to "true", the
    // find-and-replace operation will go through all the runs outside of a text box
    // before going through the ones inside a text box.
    // If we set the "UseLegacyOrder" property to "false", the
    // find-and-replace operation will go over all the runs in a range in sequential order.
    options.useLegacyOrder = useLegacyOrder;

    /* doc.range.replace(new Regex(@"\[tag \d*\]"), "", options); TODO

    Assert.AreEqual(useLegacyOrder ?
      new aw.Lists.List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
      new aw.Lists.List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches); */
  });

/*
    /// <summary>
    /// Records the order of all matches that occur during a find-and-replace operation.
    /// </summary>
  private class TextReplacementTracker : IReplacingCallback
  {
    ReplaceAction aw.Replacing.IReplacingCallback.replacing(ReplacingArgs e)
    {
      Matches.add(e.match.value);
      return aw.Replacing.ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new aw.Lists.List<string>();
  }
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

