---
title: PhysicalFontInfo class
linktitle: PhysicalFontInfo class
articleTitle: PhysicalFontInfo class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fonts.PhysicalFontInfo class. Specifies information about physical font available to Aspose.Words font engine"
type: docs
weight: 220
url: /nodejs-net/aspose.words.fonts/physicalfontinfo/
---

## PhysicalFontInfo class

Specifies information about physical font available to Aspose.Words font engine.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [embeddingLicensingRights](./embeddingLicensingRights/) | Embedding licensing rights for the font. |
| [filePath](./filePath/) | Path to the font file if any. |
| [fontFamilyName](./fontFamilyName/) | Family name of the font. |
| [fullFontName](./fullFontName/) | Full name of the font. |
| [version](./version/) | Version string of the font. |

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

* module [Aspose.Words.Fonts](../)

