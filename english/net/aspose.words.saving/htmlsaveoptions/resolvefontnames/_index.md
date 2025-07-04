---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words for .NET
description: Discover how the HtmlSaveOptions ResolveFontNames property enhances document formatting by ensuring accurate font substitutions in HTML outputs.
type: docs
weight: 430
url: /net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Specifies whether font family names used in the document are resolved and substituted according to [`FontSettings`](../../../aspose.words/document/fontsettings/) when being written into HTML-based formats.

```csharp
public bool ResolveFontNames { get; set; }
```

## Remarks

By default, this option is set to `false` and font family names are written to HTML as specified in source documents. That is, [`FontSettings`](../../../aspose.words/document/fontsettings/) are ignored and no resolution or substitution of font family names is performed.

If this option is set to `true`, Aspose.Words uses [`FontSettings`](../../../aspose.words/document/fontsettings/) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.

## Examples

Shows how to resolve all font names before writing them to HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// This document contains text that names a font that we do not have.
Assert.That(doc.FontInfos["28 Days Later"], Is.Not.Null);

// If we have no way of getting this font, and we want to be able to display all the text
// in this document in an output HTML, we can substitute it with another font.
FontSettings fontSettings = new FontSettings
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

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // By default, this option is set to 'False' and Aspose.Words writes font names as specified in the source document
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.That(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success, Is.True);
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
