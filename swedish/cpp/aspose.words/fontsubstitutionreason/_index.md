---
title: "Aspose::Words::FontSubstitutionReason enum"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FontSubstitutionReason enum. Anger orsaken till teckensnittssubstitution i C++."
type: docs
weight: 89500
url: /sv/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Anger orsaken till teckensnittssubstitution.

```cpp
enum class FontSubstitutionReason
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) substitution av alternativt namn från dokumentet. |
| FontNameSubstitutionRule | 1 | [Font](../font/) ersättning enligt regel för teckensnittsnamn. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) ersättning enligt teckensnittskonfigurationsregel. |
| TableSubstitutionRule | 3 | [Font](../font/) ersättning enligt tabellregel. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) ersättning enligt teckensnittsinformationsregel. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) ersättning enligt standardteckensnittsregel. |
| FirstAvailableFont | 6 | [Font](../font/) ersättning med det första tillgängliga teckensnittet. |


## Exempel



Visar hur man får ytterligare information om teckensnittssubstitution.
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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
