---
title: Aspose::Words::FontSubstitutionReason enum
linktitle: FontSubstitutionReason
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FontSubstitutionReason enum. Specifies the reason of font substitution in C++.'
type: docs
weight: 89500
url: /cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Specifies the reason of font substitution.

```cpp
enum class FontSubstitutionReason : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AlternativeName | 0 | Font substitution by alternative name from the document. |
| DefaultFontSubstitutionRule | 5 | Font substitution by default font rule. |
| FirstAvailableFont | 6 | Font substitution with the first available font. |
| FontConfigSubstitutionRule | 2 | Font substitution by font config rule. |
| FontInfoSubstitutionRule | 4 | Font substitution by font info rule. |
| FontNameSubstitutionRule | 1 | Font substitution by font name rule. |
| TableSubstitutionRule | 3 | Font substitution by table rule. |

## Examples


Shows how to get additional information about font substitution.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
