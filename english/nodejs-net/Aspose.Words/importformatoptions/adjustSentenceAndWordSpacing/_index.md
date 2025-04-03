---
title: ImportFormatOptions.adjustSentenceAndWordSpacing property
linktitle: adjustSentenceAndWordSpacing property
articleTitle: adjustSentenceAndWordSpacing property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.adjustSentenceAndWordSpacing property. Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically"
type: docs
weight: 20
url: /nodejs-net/aspose.words/importformatoptions/adjustSentenceAndWordSpacing/
---

## ImportFormatOptions.adjustSentenceAndWordSpacing property

Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically.
The default value is ``false``.



```js
get adjustSentenceAndWordSpacing(): boolean
```

### Examples

Shows how to adjust sentence and word spacing automatically.

```js
const srcDoc = new aw.Document();
const dstDoc = new aw.Document();

var builder = new aw.DocumentBuilder(srcDoc);
builder.write("Dolor sit amet.");

builder = new aw.DocumentBuilder(dstDoc);
builder.write("Lorem ipsum.");

const options = new aw.ImportFormatOptions();
options.adjustSentenceAndWordSpacing = true;
builder.insertDocument(srcDoc, aw.ImportFormatMode.UseDestinationStyles, options);

expect(dstDoc.firstSection.body.firstParagraph.getText().trim()).toEqual("Lorem ipsum. Dolor sit amet.");
```

### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

