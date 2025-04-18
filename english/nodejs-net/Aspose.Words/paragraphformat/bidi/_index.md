﻿---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /nodejs-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```js
get bidi(): boolean
```

### Remarks

When ``true``, the runs and other inline objects in this paragraph
are laid out right to left.




### Examples

Shows how to detect plaintext document text direction.

```js
// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
let loadOptions = new aw.Loading.TxtLoadOptions();

// Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
// the direction of every paragraph of text that Aspose.words loads from plaintext.
// Each paragraph's "Bidi" property will store its direction.
loadOptions.documentDirection = aw.Loading.DocumentDirection.Auto;

// Detect Hebrew text as right-to-left.
let doc = new aw.Document(base.myDir + "Hebrew text.txt", loadOptions);

expect(doc.firstSection.body.firstParagraph.paragraphFormat.bidi).toEqual(true);

// Detect English text as right-to-left.
doc = new aw.Document(base.myDir + "English text.txt", loadOptions);

expect(doc.firstSection.body.firstParagraph.paragraphFormat.bidi).toEqual(false);
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

