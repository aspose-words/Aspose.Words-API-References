---
title: LoadOptions.fontSettings property
linktitle: fontSettings property
articleTitle: fontSettings property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.fontSettings property. Allows to specify document font settings."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Loading/loadoptions/fontSettings/
---

## LoadOptions.fontSettings property

Allows to specify document font settings.


```js
get fontSettings(): Aspose.Words.Fonts.FontSettings
```

### Remarks

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words
may resolve the fonts to perform font fallback.

If set to ``null``, default static font settings [FontSettings.defaultInstance](../../../aspose.words.fonts/fontsettings/defaultInstance/) will be used.

The default value is ``null``.




### Examples

Shows how to apply font substitution settings while loading a document.

```js
// Create a FontSettings object that will substitute the "Times New Roman" font
// with the font "Arvo" from our "MyFonts" folder.
let fontSettings = new aw.Fonts.FontSettings();
fontSettings.setFontsFolder(base.fontsDir, false);
fontSettings.substitutionSettings.tableSubstitution.addSubstitutes("Times New Roman", [ "Arvo" ]);

// Set that FontSettings object as a property of a newly created LoadOptions object.
let loadOptions = new aw.Loading.LoadOptions();
loadOptions.fontSettings = fontSettings;

// Load the document, then render it as a PDF with the font substitution.
let doc = new aw.Document(base.myDir + "Document.docx", loadOptions);

doc.save(base.artifactsDir + "LoadOptions.fontSettings.pdf");
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

