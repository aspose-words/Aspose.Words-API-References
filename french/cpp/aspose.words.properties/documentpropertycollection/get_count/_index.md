---
title: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Properties::DocumentPropertyCollection::get_Count. Obtient le nombre d'éléments dans la collection en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


Obtient le nombre d'éléments dans la collection.

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


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

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
