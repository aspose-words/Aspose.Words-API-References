---
title: "Aspose::Words::WarningInfo::get_Description méthode"
linktitle: "get_Description"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WarningInfo::get_Description méthode. Retourne la description de l'avertissement en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/warninginfo/get_description/
---
## WarningInfo::get_Description method


Renvoie la description de l'avertissement.

```cpp
System::String Aspose::Words::WarningInfo::get_Description() const
```


## Exemples



Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante parmi les sources de police disponibles.
```cpp
// Ouvrez un document contenant du texte formaté avec une police qui n'existe dans aucune de nos sources de police.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Attribuez un rappel pour gérer les avertissements de substitution de police.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Définissez un nom de police par défaut et activez la substitution de police.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Les métriques de police d'origine doivent être utilisées après la substitution de police.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Nous recevrons un avertissement de substitution de police si nous enregistrons un document avec une police manquante.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```


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

* Class [WarningInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
