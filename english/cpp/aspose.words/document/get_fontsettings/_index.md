---
title: get_FontSettings
second_title: Aspose.Words for C++ API Reference
description: Gets or sets document font settings.
type: docs
weight: 313
url: /cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Gets or sets document font settings.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Remarks


This property allows to specify font settings per document. If set to **null**, default static font settings [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) will be used.

The default value is **null**.

## Examples



Shows how set font substitution rules. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

ArrayPtr<SharedPtr<FontSourceBase>> fontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

// The default font sources contain the first font that the document uses.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));

// The second font, "Amethysta", is unavailable.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));

// We can configure a font substitution table which determines
// which fonts Aspose.Words will use as substitutes for unavailable fonts.
// Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
// If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta",
                                                                                             MakeArray<String>({u"Arvo", u"Courier New"}));

// "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arvo"; }));

// "Arvo" is also unavailable, but "Courier New" is.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Courier New"; }));

// The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
doc->Save(ArtifactsDir + u"FontSettings.TableSubstitution.pdf");
```

## See Also

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
