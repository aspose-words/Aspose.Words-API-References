---
title: Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution method
linktitle: get_DefaultFontSubstitution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution method. Settings related to default font substitution rule in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


## Examples



Shows how to set the default font substitution rule. 
```cpp
auto doc = MakeObject<Document>();
auto fontSettings = MakeObject<FontSettings>();
doc->set_FontSettings(fontSettings);

// Get the default substitution rule within FontSettings.
// This rule will substitute all missing fonts with "Times New Roman".
SharedPtr<DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Set the default font substitute to "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Using a document builder, add some text in a font that we do not have to see the substitution take place,
// and then render the result in a PDF.
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(ArtifactsDir + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## See Also

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
