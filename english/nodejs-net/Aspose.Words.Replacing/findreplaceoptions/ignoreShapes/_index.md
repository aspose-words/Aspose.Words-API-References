---
title: FindReplaceOptions.ignoreShapes property
linktitle: ignoreShapes property
articleTitle: ignoreShapes property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreShapes property. Gets or sets a boolean value indicating either to ignore shapes within a text."
type: docs
weight: 110
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/ignoreShapes/
---

## FindReplaceOptions.ignoreShapes property

Gets or sets a boolean value indicating either to ignore shapes within a text.

The default value is ``false``.




```js
get ignoreShapes(): boolean
```

### Examples

Shows how to ignore shapes while replacing text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.insertShape(aw.Drawing.ShapeType.Balloon, 200, 200);
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

let findReplaceOptions = new aw.Replacing.FindReplaceOptions();
findReplaceOptions.ignoreShapes = true;
builder.document.range.replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
expect(builder.document.getText().trim()).toEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

