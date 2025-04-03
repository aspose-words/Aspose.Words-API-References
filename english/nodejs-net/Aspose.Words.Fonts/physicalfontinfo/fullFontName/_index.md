---
title: PhysicalFontInfo.fullFontName property
linktitle: fullFontName property
articleTitle: fullFontName property
second_title: Aspose.Words for NodeJs
description: "PhysicalFontInfo.fullFontName property. Full name of the font."
type: docs
weight: 40
url: /nodejs-net/aspose.words.fonts/physicalfontinfo/fullFontName/
---

## PhysicalFontInfo.fullFontName property

Full name of the font.


```js
get fullFontName(): string
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

