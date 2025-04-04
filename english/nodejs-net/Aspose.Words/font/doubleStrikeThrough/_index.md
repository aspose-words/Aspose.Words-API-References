---
title: Font.doubleStrikeThrough property
linktitle: doubleStrikeThrough property
articleTitle: doubleStrikeThrough property
second_title: Aspose.Words for Node.js
description: "Font.doubleStrikeThrough property. True if the font is formatted as double strikethrough text."
type: docs
weight: 90
url: /nodejs-net/aspose.words/font/doubleStrikeThrough/
---

## Font.doubleStrikeThrough property

True if the font is formatted as double strikethrough text.


```js
get doubleStrikeThrough(): boolean
```

### Examples

Shows how to add a line strikethrough to text.

```js
let doc = new aw.Document();
let para = doc.getParagraph(0, true);

let run = new aw.Run(doc, "Text with a single-line strikethrough.");
run.font.strikeThrough = true;
para.appendChild(run);

para = para.parentNode.appendChild(new aw.Paragraph(doc)).asParagraph();

run = new aw.Run(doc, "Text with a double-line strikethrough.");
run.font.doubleStrikeThrough = true;
para.appendChild(run);

doc.save(base.artifactsDir + "Font.strikeThrough.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

