---
title: FontSettings.defaultInstance property
linktitle: defaultInstance property
articleTitle: defaultInstance property
second_title: Aspose.Words for Node.js
description: "FontSettings.defaultInstance property. Static default font settings."
type: docs
weight: 20
url: /nodejs-net/aspose.words.fonts/fontsettings/defaultInstance/
---

## FontSettings.defaultInstance property

Static default font settings.


```js
get defaultInstance(): Aspose.Words.Fonts.FontSettings
```

### Remarks

This instance is used by default in a document unless [Document.fontSettings](../../../aspose.words/document/fontSettings/) is specified.



### Examples

Shows how to configure the default font settings instance.

```js
// Configure the default font settings instance to use the "Courier New" font
// as a backup substitute when we attempt to use an unknown font.
aw.Fonts.FontSettings.defaultInstance.substitutionSettings.defaultFontSubstitution.defaultFontName = "Courier New";

expect(aw.Fonts.FontSettings.defaultInstance.substitutionSettings.defaultFontSubstitution.enabled).toEqual(true);

let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Non-existent font";
builder.write("Hello world!");

// This document does not have a FontSettings configuration. When we render the document,
// the default FontSettings instance will resolve the missing font.
// Aspose.words will use "Courier New" to render text that uses the unknown font.
expect(doc.fontSettings).toBe(null);

doc.save(base.artifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

### See Also

* module [Aspose.Words.Fonts](../../)
* class [FontSettings](../)

