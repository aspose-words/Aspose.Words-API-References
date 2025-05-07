---
title: Font.allCaps property
linktitle: allCaps property
articleTitle: allCaps property
second_title: Aspose.Words for Node.js
description: "Font.allCaps property. True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /nodejs-net/aspose.words/font/allCaps/
---

## Font.allCaps property

True if the font is formatted as all capital letters.


```js
get allCaps(): boolean
```

### Examples

Shows how to format a run to display its contents in capitals.

```js
let doc = new aw.Document();
let para = doc.getParagraph(0, true);

// There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
// 1 -  Set the AllCaps flag to display all characters in regular capitals:
let run = new aw.Run(doc, "all capitals");
run.font.allCaps = true;
para.appendChild(run);

para = para.parentNode.appendChild(new aw.Paragraph(doc)).asParagraph();

// 2 -  Set the SmallCaps flag to display all characters in small capitals:
// If a character is lower case, it will appear in its upper case form
// but will have the same height as the lower case (the font's x-height).
// Characters that were in upper case originally will look the same.
run = new aw.Run(doc, "Small Capitals");
run.font.smallCaps = true;
para.appendChild(run);

doc.save(base.artifactsDir + "Font.caps.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

