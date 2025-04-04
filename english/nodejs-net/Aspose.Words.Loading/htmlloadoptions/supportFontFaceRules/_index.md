---
title: HtmlLoadOptions.supportFontFaceRules property
linktitle: supportFontFaceRules property
articleTitle: supportFontFaceRules property
second_title: Aspose.Words for Node.js
description: "HtmlLoadOptions.supportFontFaceRules property. Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts"
type: docs
weight: 60
url: /nodejs-net/aspose.words.loading/htmlloadoptions/supportFontFaceRules/
---

## HtmlLoadOptions.supportFontFaceRules property

Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts.
Default value is ``false``.



```js
get supportFontFaceRules(): boolean
```

### Remarks

If this option is enabled, fonts declared in @font-face rules are loaded and embedded into the resulting document's
font definitions (see [DocumentBase.fontInfos](../../../aspose.words/documentbase/fontInfos/)). This makes the loaded fonts available for rendering but
doesn't automatically enable embedding of the fonts upon saving. In order to save the document with loaded fonts,
the [FontInfoCollection.embedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/embedTrueTypeFonts/) property of the [DocumentBase.fontInfos](../../../aspose.words/documentbase/fontInfos/)
collection should be set to ``true``.


Supported font formats are TTF, EOT, and WOFF.

@font-face rules are not supported when loading SVG images.




### See Also

* module [Aspose.Words.Loading](../../)
* class [HtmlLoadOptions](../)

