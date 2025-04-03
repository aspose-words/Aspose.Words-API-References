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
The default value is ``false``.



```js
get allowEmbeddingPostScriptFonts(): boolean
```

### Remarks

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.embedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/embedTrueTypeFonts/) of the
[DocumentBase.fontInfos](../../../aspose.words/documentbase/fontInfos/) property is set to ``true``.




### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

