---
title: PhysicalFontInfo.fontFamilyName property
linktitle: fontFamilyName property
articleTitle: fontFamilyName property
second_title: Aspose.Words for Node.js
description: "PhysicalFontInfo.fontFamilyName property. Family name of the font."
type: docs
weight: 30
url: /nodejs-net/aspose.words.fonts/physicalfontinfo/fontFamilyName/
---

## PhysicalFontInfo.fontFamilyName property

Family name of the font.


```js
get fontFamilyName(): string
```

### Examples

Shows how to list available fonts.

```js
// Configure Aspose.words to source fonts from a custom folder, and then print every available font.
let folderFontSource = [new aw.Fonts.FolderFontSource(base.fontsDir, true)];

for (let fontInfo of folderFontSource.at(0).getAvailableFonts())
{
  console.log("FontFamilyName : {0}", fontInfo.fontFamilyName);
  console.log("FullFontName  : {0}", fontInfo.fullFontName);
  console.log("Version  : {0}", fontInfo.version);
  console.log("FilePath : {0}\n", fontInfo.filePath);
}
```

### See Also

* module [Aspose.Words.Fonts](../../)
* class [PhysicalFontInfo](../)

