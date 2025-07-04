---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words for .NET
description: Discover HtmlLoadOptions SupportFontFaceRules, control font loading with ease. Enhance your web design by enabling custom fonts for a polished look.
type: docs
weight: 60
url: /net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is `false`.

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Remarks

If this option is enabled, fonts declared in @font-face rules are loaded and embedded into the resulting document's font definitions (see [`FontInfos`](../../../aspose.words/documentbase/fontinfos/)). This makes the loaded fonts available for rendering but doesn't automatically enable embedding of the fonts upon saving. In order to save the document with loaded fonts, the [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) property of the [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) collection should be set to `true`.

Supported font formats are TTF, EOT, and WOFF.

@font-face rules are not supported when loading SVG images.

## Examples

Shows how to load declared "@font-face" rules.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.That(doc.FontInfos[0].Name, Is.EqualTo("Squarish Sans CT Regular"));
```

### See Also

* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
