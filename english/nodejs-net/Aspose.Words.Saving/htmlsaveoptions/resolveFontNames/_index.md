---
title: HtmlSaveOptions.resolveFontNames property
linktitle: resolveFontNames property
articleTitle: resolveFontNames property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.resolveFontNames property. Specifies whether font family names used in the document are resolved and substituted according to [Document.fontSettings](../../../aspose.words/document/fontSettings/) when being written into HTML-based formats."
type: docs
weight: 420
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/resolveFontNames/
---

## HtmlSaveOptions.resolveFontNames property

Specifies whether font family names used in the document are resolved and substituted according to
[Document.fontSettings](../../../aspose.words/document/fontSettings/) when being written into HTML-based formats.



```js
get resolveFontNames(): boolean
```

### Remarks

By default, this option is set to ``false`` and font family names are written to HTML as specified
in source documents. That is, [Document.fontSettings](../../../aspose.words/document/fontSettings/) are ignored and no resolution or substitution
of font family names is performed.

If this option is set to ``true``, Aspose.Words uses [Document.fontSettings](../../../aspose.words/document/fontSettings/) to resolve
each font family name specified in a source document into the name of an available font family, performing
font substitution as required.




### Examples

Shows how to resolve all font names before writing them to HTML.

```js
let doc = new aw.Document(base.myDir + "Missing font.docx");

// This document contains text that names a font that we do not have.
expect(doc.fontInfos.at("28 Days Later")).not.toBe(null);

// If we have no way of getting this font, and we want to be able to display all the text
// in this document in an output HTML, we can substitute it with another font.
let fontSettings = new aw.Fonts.FontSettings
{
  SubstitutionSettings =
  {
    DefaultFontSubstitution =
    {
      DefaultFontName = "Arial",
      Enabled = true
    }
  }
};

doc.fontSettings = fontSettings;

let saveOptions = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html)
{
  // By default, this option is set to 'False' and Aspose.words writes font names as specified in the source document
  ResolveFontNames = resolveFontNames
};

doc.save(base.artifactsDir + "HtmlSaveOptions.resolveFontNames.html", saveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.resolveFontNames.html").toString();

Assert.true(resolveFontNames
  ? Regex.match(outDocContents, "<span style=\"font-family:Arial\">").Success
  : Regex.match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

