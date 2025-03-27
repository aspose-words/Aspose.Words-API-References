---
title: ParagraphFormat.wordWrap property
linktitle: wordWrap property
articleTitle: wordWrap property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.wordWrap property. If this property is ``False``, Latin text in the middle of a word can be wrapped for the current paragraph"
type: docs
weight: 420
url: /nodejs-net/Aspose.Words/paragraphformat/wordWrap/
---

## ParagraphFormat.wordWrap property

If this property is ``False``, Latin text in the middle of a word can be wrapped for
the current paragraph. Otherwise Latin text is wrapped by whole words.



```js
get wordWrap(): boolean
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

