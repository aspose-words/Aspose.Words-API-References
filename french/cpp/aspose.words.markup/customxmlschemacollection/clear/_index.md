---
title: "Méthode Aspose::Words::Markup::CustomXmlSchemaCollection::Clear"
linktitle: "Clear"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::CustomXmlSchemaCollection::Clear. Supprime tous les éléments de la collection en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.markup/customxmlschemacollection/clear/
---
## CustomXmlSchemaCollection::Clear method


Supprime tous les éléments de la collection.

```cpp
void Aspose::Words::Markup::CustomXmlSchemaCollection::Clear()
```


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

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
