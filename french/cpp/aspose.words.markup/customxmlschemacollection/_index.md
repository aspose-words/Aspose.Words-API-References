---
title: "Classe Aspose::Words::Markup::CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Markup::CustomXmlSchemaCollection. Une collection de chaînes représentant des schémas XML associés à une partie XML personnalisée. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


Une collection de chaînes qui représentent des schémas XML associés à une partie XML personnalisée. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::String\&) | Ajoute un élément à la collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [Clone](./clone/)() | Crée une copie profonde de cet objet. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit l'élément à l'index spécifié. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Obtient ou définit l'élément à l'index spécifié. |
| [IndexOf](./indexof/)(const System::String\&) | Renvoie l'index basé sur zéro de la valeur spécifiée dans la collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Supprime la valeur spécifiée de la collection. |
| [RemoveAt](./removeat/)(int32_t) | Supprime une valeur à l'index spécifié. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarques


Vous ne créez pas d'instances de cette classe. Vous accédez à la collection de schémas XML d'une partie XML personnalisée via la propriété [Schemas](../customxmlpart/get_schemas/).

## Exemples



Montre comment travailler avec une collection de schémas XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Ajoutez une association de schéma XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clonez la collection d'associations de schémas XML de la partie XML personnalisée,
// et ajoutez ensuite quelques nouveaux schémas au clone.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Énumérez les schémas et affichez chaque élément.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Voici trois façons de supprimer des schémas de la collection.
// 1 -  Supprimer un schéma par indice :
schemas->RemoveAt(2);

// 2 -  Supprimer un schéma par valeur :
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Utilisez la méthode "Clear" pour vider la collection en une fois.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
