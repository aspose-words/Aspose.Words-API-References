---
title: DefaultFontSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: Default font substitution rule.
type: docs
weight: 1
url: /cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Default font substitution rule.

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Methods

| Method | Description |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Gets or sets the default font name. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifies whether the rule is enabled or not. |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Setter for [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Setter for [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |

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

