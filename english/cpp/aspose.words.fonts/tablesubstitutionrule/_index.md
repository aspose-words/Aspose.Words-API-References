---
title: Aspose::Words::Fonts::TableSubstitutionRule class
linktitle: TableSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::TableSubstitutionRule class. Table font substitution rule. To learn more, visit the Working with Fonts documentation article in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Table font substitution rule. 
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class TableSubstitutionRule : public FontSubstitutionRule
```

## Methods

| Method | Description |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String \&, const System::ArrayPtr\<System::String\> \&) | Adds substitute font names for given original font name. |
| [GetSubstitutes](./getsubstitutes/)(const System::String \&) | Returns array containing substitute font names for the specified original font name. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\> \&) | Loads table substitution settings from XML stream. |
| [Load](./load/)(const System::String \&) | Loads table substitution settings from XML file. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Loads predefined table substitution settings for Android platform. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Loads predefined table substitution settings for Linux platform. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Loads predefined table substitution settings for Windows platform. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\> \&) | Saves the current table substitution settings to stream. |
| [Save](./save/)(const System::String \&) | Saves the current table substitution settings to file. |
| [SetSubstitutes](./setsubstitutes/)(const System::String \&, const System::ArrayPtr\<System::String\> \&) | Override substitute font names for given original font name. |
| static [Type](./type/)() |  |
| [GetType](../fontsubstitutionrule/gettype/)() const override |  |
| [Is](../fontsubstitutionrule/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../fontsubstitutionrule/type/)() |  |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifies whether the rule is enabled or not. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Specifies whether the rule is enabled or not. |
## Remarks

 This rule defines the list of substitute font names to be used if the original font is not available. Substitutes will be checked for the font name and the [AltName](../fontinfo/get_altname/) (if any). 
## Examples


Shows how to access font substitution tables for Windows and Linux.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Create a new table substitution rule and load the default Microsoft Windows font substitution table.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// We can save the table in the form of an XML document.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux has its own substitution table.
// There are multiple substitute fonts for "Times New Roman CE".
// If the first substitute, "FreeSerif" is also unavailable,
// this rule will cycle through the others in the array until it finds an available one.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Save the Linux substitution table in the form of an XML document using a stream.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```
## See Also

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
