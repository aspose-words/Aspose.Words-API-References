---
title: DocumentBase.fontInfos property
linktitle: fontInfos property
articleTitle: fontInfos property
second_title: Aspose.Words for NodeJs
description: "DocumentBase.fontInfos property. Provides access to properties of fonts used in this document."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/documentbase/fontInfos/
---

## DocumentBase.fontInfos property

Provides access to properties of fonts used in this document.


```js
get fontInfos(): Aspose.Words.Fonts.FontInfoCollection
```

### Remarks

This collection of font definitions is loaded as is from the document.
Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document.
You should only use this collection to get information about fonts that might be used in the document.




### Examples

Shows how to print the details of what fonts are present in a document.

```js
let doc = new aw.Document(base.myDir + "Embedded font.docx");

let allFonts = doc.fontInfos;
expect(allFonts.count).toEqual(5);

// Print all the used and unused fonts in the document.
for (let i = 0; i < allFonts.count; i++) {
  console.log(`Font index #${i}`);
  console.log(`\tName: ${allFonts.at(i).name}`);
  console.log(`\tIs ${allFonts.at(i).isTrueType ? "" : "not "}a trueType font`);
}
```

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

* module [Aspose.Words](../../)
* class [DocumentBase](../)
* class [FontInfoCollection](../../../Aspose.Words.Fonts/fontinfocollection/)
* class [FontInfo](../../../Aspose.Words.Fonts/fontinfo/)

