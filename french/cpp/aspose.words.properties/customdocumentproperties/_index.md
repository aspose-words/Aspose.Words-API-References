---
title: "Aspose::Words::Properties::CustomDocumentProperties class"
linktitle: "CustomDocumentProperties"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::CustomDocumentProperties class. Une collection de propriétés de document personnalisées. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


Une collection de propriétés de document personnalisées. Pour en savoir plus, consultez l’article de documentation [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Crée une nouvelle propriété de document personnalisée du type de données [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | Crée une nouvelle propriété de document personnalisée du type de données [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | Crée une nouvelle propriété de document personnalisée du type de données [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | Crée une nouvelle propriété de document personnalisée du type de données [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | Crée une nouvelle propriété de document personnalisée du type de données [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | Crée une nouvelle propriété de document personnalisée liée au contenu. |
| [Clear](../documentpropertycollection/clear/)() | Supprime toutes les propriétés de la collection. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Renvoie **true** si une propriété portant le nom spécifié existe dans la collection. |
| [get_Count](../documentpropertycollection/get_count/)() | Obtient le nombre d'éléments dans la collection. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Renvoie un objet [DocumentProperty](../documentproperty/) par le nom de la propriété. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Renvoie un objet [DocumentProperty](../documentproperty/) par indice. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Obtient l'indice d'une propriété par son nom. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Supprime une propriété portant le nom spécifié de la collection. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Supprime une propriété à l'indice spécifié. |
| static [Type](./type/)() |  |
## Remarques


Chaque objet [DocumentProperty](../documentproperty/) représente une propriété personnalisée d'un document conteneur.

Les noms des propriétés ne sont pas sensibles à la casse.

Les propriétés de la collection sont triées alphabétiquement par nom.

## Exemples



Montre comment travailler avec les propriétés de document personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Chaque document contient une collection de propriétés personnalisées qui, comme les propriétés intégrées, sont des paires clé-valeur.
// Le document possède une liste fixe de propriétés intégrées. L'utilisateur crée toutes les propriétés personnalisées.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## Voir aussi

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
