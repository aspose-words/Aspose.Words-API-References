---
title: FontInfo.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "FontInfo.name property. Gets the name of the font."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Fonts/fontinfo/name/
---

## FontInfo.name property

Gets the name of the font.


```js
get name(): string
```

### Remarks

Cannot be ``None``. Can be an empty string.




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

