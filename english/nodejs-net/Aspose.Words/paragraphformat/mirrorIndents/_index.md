---
title: ParagraphFormat.mirrorIndents property
linktitle: mirrorIndents property
articleTitle: mirrorIndents property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.mirrorIndents property. Gets or sets a flag indicating whether the left and right indents are of the same width."
type: docs
weight: 240
url: /nodejs-net/aspose.words/paragraphformat/mirrorIndents/
---

## ParagraphFormat.mirrorIndents property

Gets or sets a flag indicating whether the left and right indents are of the same width.


```js
get mirrorIndents(): boolean
```

### Examples

Show how to make left and right indents the same.

```js
let doc = new aw.Document(base.myDir + "Document.docx");
let format = doc.firstSection.body.paragraphs.at(0).paragraphFormat;

format.mirrorIndents = true;

doc.save(base.artifactsDir + "ParagraphFormat.mirrorIndents.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

