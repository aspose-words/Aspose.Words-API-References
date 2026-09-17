---
title: "Énum Aspose::Words::WarningType"
linktitle: "WarningType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énum Aspose::Words::WarningType. Spécifie le type d'avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement d'un document en C++."
type: docs
weight: 129000
url: /fr/cpp/aspose.words/warningtype/
---
## WarningType enum


Spécifie le type d'avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document.

```cpp
enum class WarningType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| DataLossCategory | 255 | Certain texte/caractère/image ou d'autres données seront manquants soit dans l'arbre du document après le chargement, soit dans le document créé après l'enregistrement. |
| DataLoss | 1 | Perte de données générique, aucun code spécifique. |
| MajorFormattingLossCategory | 65280 | Le document résultant ou un emplacement particulier dans celui-ci peut sembler sensiblement différent du document original. |
| MajorFormattingLoss | 256 | Perte de mise en forme majeure générique, aucun code spécifique. |
| MinorFormattingLossCategory | 16711680 | Le document résultant ou un emplacement particulier dans celui-ci peut sembler quelque peu différent du document original. |
| MinorFormattingLoss | 65536 | Perte de formatage mineure générique, aucun code spécifique. |
| FontSubstitution | 131072 | [Font](../font/) a été substitué. |
| FontEmbedding | 262144 | Perte d'informations de police incorporée lors de l'enregistrement du document. |
| UnexpectedContentCategory | 251658240 | Certaines parties du document source n'ont pas pu être reconnues (c.-à-d. ne sont pas prises en charge), cela peut ou non entraîner des problèmes ou entraîner une perte de données/de formatage. |
| UnexpectedContent | 16777216 | Contenu inattendu générique, aucun code spécifique. |
| Indice | 268435456 | Indique un problème potentiel ou suggère une amélioration. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
