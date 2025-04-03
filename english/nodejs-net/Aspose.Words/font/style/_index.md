---
title: Font.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for NodeJs
description: "Font.style property. Gets or sets the character style applied to this formatting."
type: docs
weight: 410
url: /nodejs-net/aspose.words/font/style/
---

## Font.style property

Gets or sets the character style applied to this formatting.


```js
get style(): Aspose.Words.Style
```

### Examples

Applies a double underline to all runs in a document that are formatted with custom character styles.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a custom style and apply it to text created using a document builder.
let style = doc.styles.add(aw.StyleType.Character, "MyStyle");
style.font.color = "#FF0000";
style.font.name = "Courier New";

builder.font.styleName = "MyStyle";
builder.write("This text is in a custom style.");

// Iterate over every run and add a double underline to every custom style.
for (let run of doc.getChildNodes(aw.NodeType.Run, true).toArray().map(node => node.asRun()))
{
  let charStyle = run.font.style;

  if (!charStyle.builtIn)
    run.font.underline = aw.Underline.Double;
}

doc.save(base.artifactsDir + "Font.style.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

