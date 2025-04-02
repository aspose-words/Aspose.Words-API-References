---
title: DocumentBuilder.underline property
linktitle: underline property
articleTitle: underline property
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.underline property. Gets/sets underline type for the current font."
type: docs
weight: 190
url: /nodejs-net/Aspose.Words/documentbuilder/underline/
---

## DocumentBuilder.underline property

Gets/sets underline type for the current font.


```js
get underline(): Aspose.Words.Underline
```

### Examples

Shows how to format text inserted by a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.underline = aw.Underline.Dash;
builder.font.color = "#0000FF";
builder.font.size = 32;

// The builder applies formatting to its current paragraph and any new text added by it afterward.
builder.writeln("Large, blue, and underlined text.");

doc.save(base.artifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

