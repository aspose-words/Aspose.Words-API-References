---
title: ParagraphFormat.linesToDrop property
linktitle: linesToDrop property
articleTitle: linesToDrop property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.linesToDrop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /nodejs-net/aspose.words/paragraphformat/linesToDrop/
---

## ParagraphFormat.linesToDrop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```js
get linesToDrop(): number
```

### Examples

Shows how to set the size of a drop cap.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
// which will turn it into a large capital letter that will decorate the next paragraph.
// Give this property a value of 4 to give the drop cap the height of four text lines.
builder.paragraphFormat.linesToDrop = 4;
builder.writeln("H");

// Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
// The text in this paragraph will wrap around the drop cap.
builder.paragraphFormat.linesToDrop = 0;
builder.writeln("ello world!");

doc.save(base.artifactsDir + "ParagraphFormat.linesToDrop.odt");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

