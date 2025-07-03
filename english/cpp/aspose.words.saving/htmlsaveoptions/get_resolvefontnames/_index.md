---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames method
linktitle: get_ResolveFontNames
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames method. Specifies whether font family names used in the document are resolved and substituted according to FontSettings when being written into HTML-based formats in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Specifies whether font family names used in the document are resolved and substituted according to [FontSettings](../../../aspose.words/document/get_fontsettings/) when being written into HTML-based formats.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Remarks


By default, this option is set to **false** and font family names are written to HTML as specified in source documents. That is, [FontSettings](../../../aspose.words/document/get_fontsettings/) are ignored and no resolution or substitution of font family names is performed.

If this option is set to **true**, Aspose.Words uses [FontSettings](../../../aspose.words/document/get_fontsettings/) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.

## Examples



Shows how to resolve all font names before writing them to HTML. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// This document contains text that names a font that we do not have.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// If we have no way of getting this font, and we want to be able to display all the text
// in this document in an output HTML, we can substitute it with another font.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// By default, this option is set to 'False' and Aspose.Words writes font names as specified in the source document
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
