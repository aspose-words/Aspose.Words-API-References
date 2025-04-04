---
title: Font.styleName property
linktitle: styleName property
articleTitle: styleName property
second_title: Aspose.Words for Node.js
description: "Font.styleName property. Gets or sets the name of the character style applied to this formatting."
type: docs
weight: 430
url: /nodejs-net/aspose.words/font/styleName/
---

## Font.styleName property

Gets or sets the name of the character style applied to this formatting.


```js
get styleName(): string
```

### Examples

Shows how to change the style of existing text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two ways of referencing styles.
// 1 -  Using the style name:
builder.font.styleName = "Emphasis";
builder.writeln("Text originally in \"Emphasis\" style");

// 2 -  Using a built-in style identifier:
builder.font.styleIdentifier = aw.StyleIdentifier.IntenseEmphasis;
builder.writeln("Text originally in \"Intense Emphasis\" style");

// Convert all uses of one style to another,
// using the above methods to reference old and new styles.
for (let run of doc.getChildNodes(aw.NodeType.Run, true).toArray().map(node => node.asRun()))
{
  if (run.font.styleName == "Emphasis")
    run.font.styleName = "Strong";

  if (run.font.styleIdentifier == aw.StyleIdentifier.IntenseEmphasis)
    run.font.styleIdentifier = aw.StyleIdentifier.Strong;
}

doc.save(base.artifactsDir + "Font.ChangeStyle.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

