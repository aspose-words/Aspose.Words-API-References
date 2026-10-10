---
title: "Aspose::Words::FontSubstitutionReason énum"
linktitle: "FontSubstitutionReason"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FontSubstitutionReason énum. Spécifie la raison de la substitution de police en C++."
type: docs
weight: 89500
url: /fr/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Spécifie la raison de la substitution de police.

```cpp
enum class FontSubstitutionReason
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) substitution par un nom alternatif provenant du document. |
| FontNameSubstitutionRule | 1 | [Font](../font/) substitution par règle de nom de police. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) substitution par règle de configuration de police. |
| TableSubstitutionRule | 3 | [Font](../font/) substitution par règle de table. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) substitution selon la règle d'information de police. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) substitution selon la règle de police par défaut. |
| FirstAvailableFont | 6 | [Font](../font/) substitution avec la première police disponible. |


## Exemples



Montre comment obtenir des informations supplémentaires sur la substitution de police.
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

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
