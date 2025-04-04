---
title: PhysicalFontInfo.version property
linktitle: version property
articleTitle: version property
second_title: Aspose.Words for Node.js
description: "PhysicalFontInfo.version property. Version string of the font."
type: docs
weight: 50
url: /nodejs-net/aspose.words.fonts/physicalfontinfo/version/
---

## PhysicalFontInfo.version property

Version string of the font.


```js
get version(): string
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

