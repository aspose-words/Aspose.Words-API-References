---
title: DefaultFontSubstitutionRule.defaultFontName property
linktitle: defaultFontName property
articleTitle: defaultFontName property
second_title: Aspose.Words for NodeJs
description: "DefaultFontSubstitutionRule.defaultFontName property. Gets or sets the default font name."
type: docs
weight: 10
url: /nodejs-net/aspose.words.fonts/defaultfontsubstitutionrule/defaultFontName/
---

## DefaultFontSubstitutionRule.defaultFontName property

Gets or sets the default font name.


```js
get defaultFontName(): string
```

### Remarks

The default value is 'Times New Roman'.




### Examples

Shows how to specify a default font.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Arial";
builder.writeln("Hello world!");
builder.font.name = "Arvo";
builder.writeln("The quick brown fox jumps over the lazy dog.");

let fontSources = aw.Fonts.FontSettings.defaultInstance.getFontsSources();

// The font sources that the document uses contain the font "Arial", but not "Arvo".
expect(fontSources.length).toEqual(1);
expect(fontSources.at(0).getAvailableFonts().Any(f => f.fullFontName == "Arial")).toEqual(true);
expect(fontSources.at(0).getAvailableFonts().Any(f => f.fullFontName == "Arvo")).toEqual(false);

// Set the "DefaultFontName" property to "Courier New" to,
// while rendering the document, apply that font in all cases when another font is not available. 
aw.Fonts.FontSettings.defaultInstance.substitutionSettings.defaultFontSubstitution.defaultFontName = "Courier New";

expect(fontSources.at(0).getAvailableFonts().Any(f => f.fullFontName == "Courier New")).toEqual(true);

// Aspose.words will now use the default font in place of any missing fonts during any rendering calls.
doc.save(base.artifactsDir + "FontSettings.defaultFontName.pdf");
```

### See Also

* module [Aspose.Words.Fonts](../../)
* class [DefaultFontSubstitutionRule](../)

