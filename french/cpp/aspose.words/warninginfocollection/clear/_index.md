---
title: "Aspose::Words::WarningInfoCollection::Clear méthode"
linktitle: "Clear"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WarningInfoCollection::Clear méthode. Supprime tous les éléments de la collection en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/warninginfocollection/clear/
---
## WarningInfoCollection::Clear method


Supprime tous les éléments de la collection.

```cpp
void Aspose::Words::WarningInfoCollection::Clear()
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

## Voir aussi

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
