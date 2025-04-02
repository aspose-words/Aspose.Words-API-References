---
title: FontInfoCollection.embedSystemFonts property
linktitle: embedSystemFonts property
articleTitle: embedSystemFonts property
second_title: Aspose.Words for NodeJs
description: "FontInfoCollection.embedSystemFonts property. Specifies whether or not to embed System fonts into the document"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Fonts/fontinfocollection/embedSystemFonts/
---

## FontInfoCollection.embedSystemFonts property

Specifies whether or not to embed System fonts into the document.
Default value for this property is ``False``.

This option works only when [FontInfoCollection.embedTrueTypeFonts](../embedTrueTypeFonts/) option is set to ``True``.




```js
get embedSystemFonts(): boolean
```

### Remarks

Setting this property to ``True`` is useful if the user is on an East Asian system
and wants to create a document that is readable by others who do not have fonts for that
language on their system. For example, a user on a Japanese system could choose to embed the
fonts in a document so that the Japanese document would be readable on all systems.


This option works for DOC, DOCX and RTF formats only.




### Examples

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

* module [Aspose.Words.Fonts](../../)
* class [FontInfoCollection](../)

