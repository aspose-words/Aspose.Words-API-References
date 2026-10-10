---
title: "Classe Aspose::Words::WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::WarningInfoCollection. Représente une collection typée d'objets WarningInfo. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 75000
url: /fr/cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


Représente une collection typée d'objets [WarningInfo](../warninginfo/). Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient un élément à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | Implémente l'interface [IWarningCallback](../iwarningcallback/). Ajoute un avertissement à cette collection. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarques


Vous pouvez utiliser cet objet de collection comme la forme la plus simple d'implémentation de [IWarningCallback](../iwarningcallback/) pour rassembler tous les avertissements générés par Aspose.Words lors d'une opération de chargement ou d'enregistrement. Créez une instance de cette classe et affectez‑la à la propriété [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) ou [WarningCallback](../documentbase/get_warningcallback/).

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

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
