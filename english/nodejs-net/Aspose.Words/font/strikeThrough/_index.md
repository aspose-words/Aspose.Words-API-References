---
title: Font.strikeThrough property
linktitle: strikeThrough property
articleTitle: strikeThrough property
second_title: Aspose.Words for NodeJs
description: "Font.strikeThrough property. True if the font is formatted as strikethrough text."
type: docs
weight: 400
url: /nodejs-net/aspose.words/font/strikeThrough/
---

## Font.strikeThrough property

True if the font is formatted as strikethrough text.


```js
get strikeThrough(): boolean
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

