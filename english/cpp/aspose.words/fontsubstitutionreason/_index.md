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
enum class FontSubstitutionReason
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) substitution by alternative name from the document. |
| FontNameSubstitutionRule | 1 | [Font](../font/) substitution by font name rule. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) substitution by font config rule. |
| TableSubstitutionRule | 3 | [Font](../font/) substitution by table rule. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) substitution by font info rule. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) substitution by default font rule. |
| FirstAvailableFont | 6 | [Font](../font/) substitution with the first available font. |


## Examples



Shows how to get additional information about font substitution. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(Aspose::Words::WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(Aspose::Words::WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(Aspose::Words::FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
