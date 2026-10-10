---
title: "Aspose::Words::WarningInfo class"
linktitle: "WarningInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WarningInfo class. Contient des informations sur un avertissement qu'Aspose.Words a émis lors du chargement ou de l'enregistrement du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 74000
url: /fr/cpp/aspose.words/warninginfo/
---
## WarningInfo class


Contient des informations sur un avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement d'un document. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfo : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Description](./get_description/)() const | Renvoie la description de l'avertissement. |
| [get_Source](./get_source/)() const | Renvoie la source de l'avertissement. |
| [get_WarningType](./get_warningtype/)() const | Renvoie le type de l'avertissement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'instances de cette classe. Les objets de cette classe sont créés et transmis par Aspose.Words à la méthode [Warning()](../iwarningcallback/warning/).

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
