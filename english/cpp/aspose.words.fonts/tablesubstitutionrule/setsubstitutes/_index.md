---
title: SetSubstitutes
second_title: Aspose.Words for C++ API Reference
description: Override substitute font names for given original font name.
type: docs
weight: 92
url: /cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method


Override substitute font names for given original font name.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | const System::String\& | Original font name. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | List of alternative font names. |

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

