---
title: Aspose::Words::Fonts::SystemFontSource class
linktitle: SystemFontSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::SystemFontSource class. Represents all TrueType fonts installed to the system. To learn more, visit the  documentation article in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class


Represents all TrueType fonts installed to the system. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class SystemFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methods

| Method | Description |
| --- | --- |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returns the font source priority. |
| [get_Type](./get_type/)() override | Returns the type of the font source. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| static [GetSystemFontFolders](./getsystemfontfolders/)() | Returns system font folders or empty array if folders are not accessible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Fonts::FontSourceBase::get_WarningCallback](../fontsourcebase/get_warningcallback/). |
| [SystemFontSource](./systemfontsource/)() | Ctor. |
| [SystemFontSource](./systemfontsource/)(int32_t) | Ctor. |
| static [Type](./type/)() |  |

## Examples



Shows how to access a document's system font source and set font substitutes. 
```cpp
auto doc = MakeObject<Document>();
doc->set_FontSettings(MakeObject<FontSettings>());

// By default, a blank document always contains a system font source.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) ||
                 (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const String fontsPath = u"C:\\WINDOWS\\Fonts";
    ASSERT_EQ(fontsPath.ToLower(), SystemFontSource::GetSystemFontFolders()->LINQ_First().ToLower());
}

for (String systemFontFolder : SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", MakeArray<String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()
                ->get_SubstitutionSettings()
                ->get_TableSubstitution()
                ->GetSubstitutes(u"Kreon-Regular")
                ->LINQ_ToArray()
                ->Contains(u"Calibri"));

// Alternatively, we could add a folder font source in which the corresponding folder contains the font.
auto folderFontSource = MakeObject<FolderFontSource>(FontsDir, false);
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
```

## See Also

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
