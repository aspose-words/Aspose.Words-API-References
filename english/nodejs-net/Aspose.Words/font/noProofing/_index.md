---
title: Font.noProofing property
linktitle: noProofing property
articleTitle: noProofing property
second_title: Aspose.Words for Node.js
description: "Font.noProofing property. True when the formatted characters are not to be spell checked."
type: docs
weight: 280
url: /nodejs-net/aspose.words/font/noProofing/
---

## Font.noProofing property

True when the formatted characters are not to be spell checked.


```js
get noProofing(): boolean
```

### Examples

Shows how to prevent text from being spell checked by Microsoft Word.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
// We can un-set the "NoProofing" flag to create a portion of text that
// bypasses the spell checker while completely disabling it.
builder.font.noProofing = true;

builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.save(base.artifactsDir + "Font.noProofing.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

