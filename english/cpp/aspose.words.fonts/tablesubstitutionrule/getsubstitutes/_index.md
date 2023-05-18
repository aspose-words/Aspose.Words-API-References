---
title: Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes method
linktitle: GetSubstitutes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes method. Returns array containing substitute font names for the specified original font name in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule::GetSubstitutes method


Returns array containing substitute font names for the specified original font name.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerable<System::String>> Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes(const System::String &originalFontName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | const System::String\& | Original font name. |

### ReturnValue

List of alternative font names.

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


Shows how to work with custom font substitution tables. 
```cpp
auto doc = MakeObject<Document>();
auto fontSettings = MakeObject<FontSettings>();
doc->set_FontSettings(fontSettings);

// Create a new table substitution rule and load the default Windows font substitution table.
SharedPtr<TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// If we select fonts exclusively from our folder, we will need a custom substitution table.
// We will no longer have access to the Microsoft Windows fonts,
// such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
auto folderFontSource = MakeObject<FolderFontSource>(FontsDir, false);
fontSettings->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({folderFontSource}));

// Below are two ways of loading a substitution table from a file in the local file system.
// 1 -  From a stream:
{
    auto fileStream = MakeObject<System::IO::FileStream>(MyDir + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Directly from a file:
tableSubstitutionRule->Load(MyDir + u"Font substitution rules.xml");

// Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
// We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
ASPOSE_ASSERT_EQ(MakeArray<String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
ASSERT_TRUE(tableSubstitutionRule->GetSubstitutes(u"Times New Roman") == nullptr);
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", MakeArray<String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(MakeArray<String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
// In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", MakeArray<String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(MakeArray<String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() can set a new list of substitute fonts for a font.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", MakeArray<String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(MakeArray<String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Writing text in fonts that we do not have access to will invoke our substitution rules.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(ArtifactsDir + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## See Also

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
