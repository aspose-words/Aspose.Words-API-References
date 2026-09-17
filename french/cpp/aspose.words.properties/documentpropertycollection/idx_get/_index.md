---
title: "Méthode Aspose::Words::Properties::DocumentPropertyCollection::idx_get"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Properties::DocumentPropertyCollection::idx_get. Retourne un objet DocumentProperty par indice en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


Retourne un objet [DocumentProperty](../../documentproperty/) par indice.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Indice basé sur zéro du [DocumentProperty](../../documentproperty/) à récupérer. |

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

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Retourne un objet [DocumentProperty](../../documentproperty/) par le nom de la propriété.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | System::String | Le nom de la propriété à récupérer, insensible à la casse. |
## Remarques


Retourne **null** si une propriété avec le nom spécifié n'est pas trouvée.

## Exemples



Montre comment créer une propriété de document personnalisée qui contient une date et une heure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
