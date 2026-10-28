---
title: Aspose::Words::Fonts::FontInfoSubstitutionRule class
linktitle: FontInfoSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoSubstitutionRule class. Font info substitution rule. To learn more, visit the Working with Fonts documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class


Font info substitution rule. 
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontInfoSubstitutionRule : public FontSubstitutionRule
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [GetType](../fontsubstitutionrule/gettype/)() const override |  |
| [Is](../fontsubstitutionrule/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../fontsubstitutionrule/type/)() |  |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifies whether the rule is enabled or not. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Specifies whether the rule is enabled or not. |
## Remarks

 According to this rule Aspose.Words evaluates all the related fields in [FontInfo](../fontinfo/) (Panose, Sig etc) for the missing font and finds the closest match among the available font sources. If [FontInfo](../fontinfo/) is not available for the missing font then nothing will be done. 
## Examples


Shows how to set the property for finding the closest match for a missing font from the available font sources.

```cpp
// Open a document that contains text formatted with a font that does not exist in any of our font sources.
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Missing font.docx"));

// Assign a callback for handling font substitution warnings.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Set a default font name and enable font substitution.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Original font metrics should be used after font substitution.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// We will get a font substitution warning if we save a document with a missing font.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```
## See Also

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
