---
title: FindReplaceOptions.applyFont property
linktitle: applyFont property
articleTitle: applyFont property
second_title: Aspose.Words for Node.js
description: "FindReplaceOptions.applyFont property. Text formatting applied to new content."
type: docs
weight: 20
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/applyFont/
---

## FindReplaceOptions.applyFont property

Text formatting applied to new content.


```js
get applyFont(): Aspose.Words.Font
```

### Examples

Shows how to apply a different font to new content via FindReplaceOptions.

```js
test.skip('ConvertNumbersToHexadecimal - TODO: WORDSNODEJS-106 - Add support of regex to doc.range.replace', () => {
    let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);

    builder.font.name = "Arial";
    builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
            "123, 456, 789 and 17379.");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    let options = new aw.Replacing.FindReplaceOptions();

    // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
    options.applyFont.highlightColor = "#D3D3D3";

    let numberHexer = new NumberHexer();
    options.replacingCallback = numberHexer;

    let replacementCount = doc.range.replace(new Regex("[0-9]+"), "", options);

    console.log(numberHexer.GetLog());

    expect(replacementCount).toEqual(4);
    expect(doc.getText().trim()).toEqual("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
                            "0x7B, 0x1C8, 0x315 and 0x43E3.");
    expect(doc.getChildNodes(aw.NodeType.Run, true).filter(r => r.asRun().font.highlightColor == "#D3D3D3")).toEqual(4);
  });

/*
    /// <summary>
    /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
    /// Maintains a log of every replacement.
    /// </summary>
  private class NumberHexer : IReplacingCallback
  {
    public ReplaceAction Replacing(ReplacingArgs args)
    {
      mCurrentReplacementNumber++;

      int number = Convert.ToInt32(args.match.value);

      args.replacement = `0x${number:X}`;

      mLog.AppendLine(`Match #${mCurrentReplacementNumber}`);
      mLog.AppendLine(`\tOriginal value:\t${args.match.value}`);
      mLog.AppendLine(`\tReplacement:\t${args.replacement}`);
      mLog.AppendLine(`\tOffset in parent ${args.matchNode.nodeType} node:\t${args.matchOffset}`);

      mLog.AppendLine(string.IsNullOrEmpty(args.groupName)
        ? `\tGroup index:\t${args.groupIndex}`
        : `\tGroup name:\t${args.groupName}`);

      return aw.Replacing.ReplaceAction.Replace;
    }

    public string GetLog()
    {
      return mLog.toString();
    }

    private int mCurrentReplacementNumber;
    private readonly StringBuilder mLog = new StringBuilder();
  }
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

