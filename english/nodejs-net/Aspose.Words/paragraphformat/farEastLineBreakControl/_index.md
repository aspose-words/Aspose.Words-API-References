---
title: ParagraphFormat.farEastLineBreakControl property
linktitle: farEastLineBreakControl property
articleTitle: farEastLineBreakControl property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.farEastLineBreakControl property. Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph."
type: docs
weight: 110
url: /nodejs-net/aspose.words/paragraphformat/farEastLineBreakControl/
---

## ParagraphFormat.farEastLineBreakControl property

Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.


```js
get farEastLineBreakControl(): boolean
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

