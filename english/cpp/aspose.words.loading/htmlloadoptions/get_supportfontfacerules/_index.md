---
title: Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules method
linktitle: get_SupportFontFaceRules
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules method. Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is false in C++.'
type: docs
weight: 6500
url: /cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Remarks


If this option is enabled, fonts declared in @font-face rules are loaded and embedded into the resulting document's font definitions (see [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). This makes the loaded fonts available for rendering but doesn't automatically enable embedding of the fonts upon saving. In order to save the document with loaded fonts, the [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) property of the [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) collection should be set to **true**.

Supported font formats are TTF, EOT, and WOFF.

@font-face rules are not supported when loading SVG images.

## Examples



Shows how to load declared "@font-face" rules. 
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
