---
title: Font.subscript property
linktitle: subscript property
articleTitle: subscript property
second_title: Aspose.Words for Node.js
description: "Font.subscript property. True if the font is formatted as subscript."
type: docs
weight: 440
url: /nodejs-net/aspose.words/font/subscript/
---

## Font.subscript property

True if the font is formatted as subscript.


```js
get subscript(): boolean
```

### Examples

Shows how to format text to offset its position.

```js
let doc = new aw.Document();
let para = doc.getParagraph(0, true);

// Raise this run of text 5 points above the baseline.
let run = new aw.Run(doc, "Raised text. ");
run.font.position = 5;
para.appendChild(run);

// Lower this run of text 10 points below the baseline.
run = new aw.Run(doc, "Lowered text. ");
run.font.position = -10;
para.appendChild(run);

// Add a run of normal text.
run = new aw.Run(doc, "Text in its default position. ");
para.appendChild(run);

// Add a run of text that appears as subscript.
run = new aw.Run(doc, "Subscript. ");
run.font.subscript = true;
para.appendChild(run);

// Add a run of text that appears as superscript.
run = new aw.Run(doc, "Superscript.");
run.font.superscript = true;
para.appendChild(run);

doc.save(base.artifactsDir + "Font.PositionSubscript.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

