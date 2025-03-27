---
title: SaveOptions.allowEmbeddingPostScriptFonts property
linktitle: allowEmbeddingPostScriptFonts property
articleTitle: allowEmbeddingPostScriptFonts property
second_title: Aspose.Words for NodeJs
description: "SaveOptions.allowEmbeddingPostScriptFonts property. Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Saving/saveoptions/allowEmbeddingPostScriptFonts/
---

## SaveOptions.allowEmbeddingPostScriptFonts property

Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines
when embedding TrueType fonts in a document upon it is saved.
The default value is ``False``.



```js
get allowEmbeddingPostScriptFonts(): boolean
```

### Remarks

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.embedTrueTypeFonts](../../../Aspose.Words.Fonts/fontinfocollection/embedTrueTypeFonts/) of the
[DocumentBase.fontInfos](../../../Aspose.Words/documentbase/fontInfos/) property is set to ``True``.




### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

