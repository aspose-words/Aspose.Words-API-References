---
title: FontInfo class
linktitle: FontInfo class
articleTitle: FontInfo class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fonts.FontInfo class. Specifies information about a font used in the document"
type: docs
weight: 110
url: /nodejs-net/aspose.words.fonts/fontinfo/
---

## FontInfo class

Specifies information about a font used in the document.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

You do not create instances of this class directly.
Use the [DocumentBase.fontInfos](../../aspose.words/documentbase/fontInfos/) property to access the collection of fonts
defined in a document.




### Properties

| Name | Description |
| --- | --- |
| [altName](./altName/) | Gets or sets the alternate name for the font. |
| [charset](./charset/) | Gets or sets the character set for the font. |
| [embeddingLicensingRights](./embeddingLicensingRights/) | Gets the embedded font licensing rights. |
| [family](./family/) | Gets or sets the font family this font belongs to. |
| [isTrueType](./isTrueType/) | Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is ``true``. |
| [name](./name/) | Gets the name of the font. |
| [panose](./panose/) | Gets or sets the PANOSE typeface classification number. |
| [pitch](./pitch/) | The pitch indicates if the font is fixed pitch, proportionally spaced, or relies on a default setting. |

### Methods

| Name | Description |
| --- | --- |
|[ getEmbeddedFont(format, style)](./getEmbeddedFont/#embeddedfontformat_embeddedfontstyle) | Gets a specific embedded font file. |
|[ getEmbeddedFontAsOpenType(style)](./getEmbeddedFontAsOpenType/#embeddedfontstyle) | Gets an embedded font file in OpenType format. Fonts in Embedded OpenType format are converted to OpenType. |

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

* module [Aspose.Words.Fonts](../)
* class [FontInfoCollection](../fontinfocollection/)
* property [DocumentBase.fontInfos](../../aspose.words/documentbase/fontInfos/)

