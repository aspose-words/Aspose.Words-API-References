---
title: FontInfoCollection class
linktitle: FontInfoCollection class
articleTitle: FontInfoCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fonts.FontInfoCollection class. Represents a collection of fonts used in a document"
type: docs
weight: 120
url: /nodejs-net/Aspose.Words.Fonts/fontinfocollection/
---

## FontInfoCollection class

Represents a collection of fonts used in a document.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

Items are [FontInfo](../fontinfo/) objects.

You do not create instances of this class directly. 
Use the [DocumentBase.fontInfos](../../aspose.words/documentbase/fontInfos/) property to access the collection of fonts 
defined in the document.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |
| [embedSystemFonts](./embedSystemFonts/) | Specifies whether or not to embed System fonts into the document. Default value for this property is ``false``. |
| [embedTrueTypeFonts](./embedTrueTypeFonts/) | Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is ``false``. |
| [saveSubsetFonts](./saveSubsetFonts/) | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is ``false``. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ contains(name)](./contains/#string) | Determines whether the collection contains a font with the given name. |

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

* module [Aspose.Words.Fonts](../)
* class [FontInfo](../fontinfo/)
* property [DocumentBase.fontInfos](../../aspose.words/documentbase/fontInfos/)

