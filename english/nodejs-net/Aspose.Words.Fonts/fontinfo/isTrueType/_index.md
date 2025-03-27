---
title: FontInfo.isTrueType property
linktitle: isTrueType property
articleTitle: isTrueType property
second_title: Aspose.Words for NodeJs
description: "FontInfo.isTrueType property. Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font"
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Fonts/fontinfo/isTrueType/
---

## FontInfo.isTrueType property

Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font.
Default is ``True``.



```js
get isTrueType(): boolean
```

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

### See Also

* module [Aspose.Words.Fonts](../../)
* class [FontInfo](../)

