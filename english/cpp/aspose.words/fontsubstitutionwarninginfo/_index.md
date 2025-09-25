---
title: Aspose::Words::FontSubstitutionWarningInfo class
linktitle: FontSubstitutionWarningInfo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FontSubstitutionWarningInfo class. Contains information about a font substitution warning that Aspose.Words issued during document loading or saving in C++.'
type: docs
weight: 29500
url: /cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


Contains information about a font substitution warning that Aspose.Words issued during document loading or saving.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## Methods

| Method | Description |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | Returns the description of the warning. |
| [get_Reason](./get_reason/)() const | [Font](../font/) substitution reason. |
| [get_RequestedBold](./get_requestedbold/)() const | Indicates whether bold style was requested. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | Requested font family name. |
| [get_RequestedItalic](./get_requesteditalic/)() const | Indicates whether italic style was requested. |
| [get_ResolvedFont](./get_resolvedfont/)() const | Resolved font. |
| [get_Source](../warninginfo/get_source/)() const | Returns the source of the warning. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | Returns the type of the warning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
