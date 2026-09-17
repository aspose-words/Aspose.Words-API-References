---
title: "Aspose::Words::DocumentBase::get_WarningCallback méthode"
linktitle: "get_WarningCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBase::get_WarningCallback méthode. Appelé pendant diverses procédures de traitement de document lorsqu'un problème est détecté et pourrait entraîner une perte de fidélité des données ou du formatage en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/documentbase/get_warningcallback/
---
## DocumentBase::get_WarningCallback method


Appelé pendant diverses procédures de traitement de document lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::DocumentBase::get_WarningCallback() const
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

* Interface [IWarningCallback](../../iwarningcallback/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
