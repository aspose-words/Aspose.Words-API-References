---
title: Aspose::Words::Fonts::FontSubstitutionSettings class
linktitle: FontSubstitutionSettings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSubstitutionSettings class. Specifies font substitution mechanism settings. To learn more, visit the  documentation article in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


Specifies font substitution mechanism settings. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontSubstitutionSettings : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) related to default font substitution rule. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) related to font config substitution rule. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) related to font info substitution rule. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) related to font name substitution rule. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) related to table substitution rule. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

The order of the rules is following:1. [Font](../../aspose.words/font/) name substitution rule (enabled by default)
1. [Font](../../aspose.words/font/) config substitution rule (disabled by default)
1. Table substitution rule (enabled by default)
1. [Font](../../aspose.words/font/) info substitution rule (enabled by default)
1. Default font rule (enabled by default)



Note that font info substitution rule will always resolve the font if [FontInfo](../fontinfo/) is available and will override the default font rule. If you want to use the default font rule then you should disable the font info substitution rule.

Note that font config substitution rule will resolve the font in most cases and thus overrides all other rules.

## Examples



Shows how to access a document's system font source and set font substitutes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// By default, a blank document always contains a system font source.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// Alternatively, we could add a folder font source in which the corresponding folder contains the font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
