---
title: FontInfoCollection.embedTrueTypeFonts property
linktitle: embedTrueTypeFonts property
articleTitle: embedTrueTypeFonts property
second_title: Aspose.Words for NodeJs
description: "FontInfoCollection.embedTrueTypeFonts property. Specifies whether or not to embed TrueType fonts in a document when it is saved"
type: docs
weight: 30
url: /nodejs-net/aspose.words.fonts/fontinfocollection/embedTrueTypeFonts/
---

## FontInfoCollection.embedTrueTypeFonts property

Specifies whether or not to embed TrueType fonts in a document when it is saved.
Default value for this property is ``false``.



```js
get embedTrueTypeFonts(): boolean
```

### Remarks

Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it,
but may substantially increase the document size.

This option works for DOC, DOCX and RTF formats only.




### Examples

Shows how to save a document with embedded TrueType fonts.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let fontInfos = doc.fontInfos;
fontInfos.embedTrueTypeFonts = embedAllFonts;
fontInfos.embedSystemFonts = embedAllFonts;
fontInfos.saveSubsetFonts = embedAllFonts;

doc.save(base.artifactsDir + "Font.FontInfoCollection.docx");
```

### See Also

* module [Aspose.Words.Fonts](../../)
* class [FontInfoCollection](../)

