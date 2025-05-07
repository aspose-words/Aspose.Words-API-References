---
title: ParagraphFormat.hangingPunctuation property
linktitle: hangingPunctuation property
articleTitle: hangingPunctuation property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.hangingPunctuation property. Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph."
type: docs
weight: 130
url: /nodejs-net/aspose.words/paragraphformat/hangingPunctuation/
---

## ParagraphFormat.hangingPunctuation property

Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph.


```js
get hangingPunctuation(): boolean
```

### Examples

Shows how to set special properties for Asian typography.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let format = doc.firstSection.body.firstParagraph.paragraphFormat;
format.farEastLineBreakControl = true;
format.wordWrap = false;
format.hangingPunctuation = true;

doc.save(base.artifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

