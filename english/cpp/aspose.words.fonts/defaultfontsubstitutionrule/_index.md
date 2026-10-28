---
title: Aspose::Words::Fonts::DefaultFontSubstitutionRule class
linktitle: DefaultFontSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::DefaultFontSubstitutionRule class. Default font substitution rule. To learn more, visit the Working with Fonts documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Default font substitution rule. 
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class DefaultFontSubstitutionRule : public FontSubstitutionRule
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_DefaultFontName](./get_defaultfontname/)() | Gets or sets the default font name. |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String \&) | Sets the default font name. |
| [GetType](../fontsubstitutionrule/gettype/)() const override |  |
| [Is](../fontsubstitutionrule/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../fontsubstitutionrule/type/)() |  |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifies whether the rule is enabled or not. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Specifies whether the rule is enabled or not. |
## Remarks

 This rule defines single default font name to be used for substitution if the original font is not available. 
## Examples


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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
