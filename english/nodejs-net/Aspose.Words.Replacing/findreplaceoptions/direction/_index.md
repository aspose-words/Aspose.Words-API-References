---
title: FindReplaceOptions.direction property
linktitle: direction property
articleTitle: direction property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.direction property. Selects direction for replace"
type: docs
weight: 40
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/direction/
---

## FindReplaceOptions.direction property

Selects direction for replace. Default value is [FindReplaceDirection.Forward](../../findreplacedirection/#Forward).



```js
get direction(): Aspose.Words.Replacing.FindReplaceDirection
```

### Examples

Shows how to determine which direction a find-and-replace operation traverses the document in.

```js
test.skip.each([aw.Replacing.FindReplaceDirection.Backward,
    aw.Replacing.FindReplaceDirection.Forward])('Direction - TODO: WORDSNODEJS-106 - Add support of regex to doc.range.replace', (findReplaceDirection) => {
    let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);

    // Insert three runs which we can search for using a regex pattern.
    // Place one of those runs inside a text box.
    builder.writeln("Match 1.");
    builder.writeln("Match 2.");
    builder.writeln("Match 3.");
    builder.writeln("Match 4.");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    let options = new aw.Replacing.FindReplaceOptions();

    // Assign a custom callback to the "ReplacingCallback" property.
    let callback = new TextReplacementRecorder();
    options.replacingCallback = callback;

    // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
    // operation to start from the end of the range, and traverse back to the beginning.
    // Set the "Direction" property to "FindReplaceDirection.Forward" to get the find-and-replace
    // operation to start from the beginning of the range, and traverse to the end.
    options.direction = findReplaceDirection;

    // TODO doc.range.replace(new Regex(@"Match \d*"), "Replacement", options);

    expect(doc.getText().trim()).toEqual("Replacement.\r" +
                            "Replacement.\r" +
                            "Replacement.\r" +
                            "Replacement.");

    switch (findReplaceDirection)
    {
      case aw.Replacing.FindReplaceDirection.Forward:
        expect(callback.Matches).toEqual(["Match 1", "Match 2", "Match 3", "Match 4"]);
        break;
      case aw.Replacing.FindReplaceDirection.Backward:
        expect(callback.Matches).toEqual(["Match 4", "Match 3", "Match 2", "Match 1"]);
        break;
    }
  });

/*
    /// <summary>
    /// Records all matches that occur during a find-and-replace operation in the order that they take place.
    /// </summary>
  private class TextReplacementRecorder : IReplacingCallback
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

