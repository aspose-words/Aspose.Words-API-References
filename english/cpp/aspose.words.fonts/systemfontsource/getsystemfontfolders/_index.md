---
title: Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders method
linktitle: GetSystemFontFolders
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders method. Returns system font folders or empty array if folders are not accessible in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.fonts/systemfontsource/getsystemfontfolders/
---
## SystemFontSource::GetSystemFontFolders method


Returns system font folders or empty array if folders are not accessible.

```cpp
static System::ArrayPtr<System::String> Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()
```

## Remarks

 On some platforms Aspose.Words could search system fonts not only through folders but in other sources too. For example, on Windows platform Aspose.Words search fonts also in the registry. 
## Examples


Shows how to access a document's system font source and set font substitutes.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// By default, a blank document always contains a system font source.
ASSERT_EQ(doc->get_FontSettings()->GetFontsSources()->get_Length(), 1);

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()[0]);
ASSERT_EQ(systemFontSource->get_Type(), FontSourceType::SystemFonts);
ASSERT_EQ(systemFontSource->get_Priority(), 0);

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    ASSERT_EQ(System::SafeInvoke(SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault(), [&](auto&& expr){return expr.ToLower();}), fontsPath.ToLower());
}

for (System::String systemFontFolder : SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({
    u"Calibri"}));

ASSERT_EQ(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count(), 1);
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// Alternatively, we could add a folder font source in which the corresponding folder contains the font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(doc->get_FontSettings()->GetFontsSources()->get_Length(), 2);

// Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(doc->get_FontSettings()->GetFontsSources()->get_Length(), 1);
ASSERT_EQ(doc->get_FontSettings()->GetFontsSources()[0]->get_Type(), FontSourceType::SystemFonts);
ASSERT_EQ(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count(), 1);
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```
## See Also

* Class [SystemFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
