---
title: FontInfoCollection.saveSubsetFonts property
linktitle: saveSubsetFonts property
articleTitle: saveSubsetFonts property
second_title: Aspose.Words for NodeJs
description: "FontInfoCollection.saveSubsetFonts property. Specifies whether or not to save a subset of the embedded TrueType fonts with the document"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Fonts/fontinfocollection/saveSubsetFonts/
---

## FontInfoCollection.saveSubsetFonts property

Specifies whether or not to save a subset of the embedded TrueType fonts with the document.
Default value for this property is ``False``.

This option works only when [FontInfoCollection.embedTrueTypeFonts](../embedTrueTypeFonts/) property is set to ``True``.




```js
get saveSubsetFonts(): boolean
```

### Remarks

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

