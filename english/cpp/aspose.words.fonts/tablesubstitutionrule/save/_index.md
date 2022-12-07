---
title: Save
second_title: Aspose.Words for C++ API Reference
description: Saves the current table substitution settings to stream.
type: docs
weight: 118
url: /cpp/aspose.words.fonts/tablesubstitutionrule/save/
---
## TableSubstitutionRule::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Saves the current table substitution settings to stream.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Output stream. |

## Examples



Shows how to access font substitution tables for Windows and Linux. 
```cpp
auto doc = MakeObject<Document>();
auto fontSettings = MakeObject<FontSettings>();
doc->set_FontSettings(fontSettings);

// Create a new table substitution rule and load the default Microsoft Windows font substitution table.
SharedPtr<TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
ASPOSE_ASSERT_EQ(MakeArray<String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// We can save the table in the form of an XML document.
tableSubstitutionRule->Save(ArtifactsDir + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux has its own substitution table.
// There are multiple substitute fonts for "Times New Roman CE".
// If the first substitute, "FreeSerif" is also unavailable,
// this rule will cycle through the others in the array until it finds an available one.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(MakeArray<String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}),
                 tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Save the Linux substitution table in the form of an XML document using a stream.
{
    auto fileStream = MakeObject<System::IO::FileStream>(ArtifactsDir + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## See Also

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
## TableSubstitutionRule::Save(const System::String\&) method


Saves the current table substitution settings to file.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Output file name. |

## Examples



Shows how to access font substitution tables for Windows and Linux. 
```cpp
auto doc = MakeObject<Document>();
auto fontSettings = MakeObject<FontSettings>();
doc->set_FontSettings(fontSettings);

// Create a new table substitution rule and load the default Microsoft Windows font substitution table.
SharedPtr<TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
ASPOSE_ASSERT_EQ(MakeArray<String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// We can save the table in the form of an XML document.
tableSubstitutionRule->Save(ArtifactsDir + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux has its own substitution table.
// There are multiple substitute fonts for "Times New Roman CE".
// If the first substitute, "FreeSerif" is also unavailable,
// this rule will cycle through the others in the array until it finds an available one.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(MakeArray<String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}),
                 tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Save the Linux substitution table in the form of an XML document using a stream.
{
    auto fileStream = MakeObject<System::IO::FileStream>(ArtifactsDir + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## See Also

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
