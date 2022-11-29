---
title: Load
second_title: Aspose.Words for C++ API Reference
description: Loads table substitution settings from XML stream.
type: docs
weight: 27
url: /cpp/aspose.words.fonts/tablesubstitutionrule/load/
---
## TableSubstitutionRule::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


Loads table substitution settings from XML stream.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Input stream. |

## Examples



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
* Library [Aspose.Words](../../../)
## TableSubstitutionRule::Load(const System::String\&) method


Loads table substitution settings from XML file.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Load(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Input file name. |

## Examples



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
* Library [Aspose.Words](../../../)
