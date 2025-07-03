---
title: Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName method
linktitle: get_DefaultFontName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName method. Gets or sets the default font name in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/defaultfontsubstitutionrule/get_defaultfontname/
---
## DefaultFontSubstitutionRule::get_DefaultFontName method


Gets or sets the default font name.

```cpp
System::String Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName()
```

## Remarks


The default value is 'Times New Roman'.

## Examples



Shows how to specify a default font. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// The font sources that the document uses contain the font "Arial", but not "Arvo".
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// Set the "DefaultFontName" property to "Courier New" to,
// while rendering the document, apply that font in all cases when another font is not available.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Aspose.Words will now use the default font in place of any missing fonts during any rendering calls.
doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontName.pdf");
```


Shows how to set the default font substitution rule. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Get the default substitution rule within FontSettings.
// This rule will substitute all missing fonts with "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Set the default font substitute to "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Using a document builder, add some text in a font that we do not have to see the substitution take place,
// and then render the result in a PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## See Also

* Class [DefaultFontSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
