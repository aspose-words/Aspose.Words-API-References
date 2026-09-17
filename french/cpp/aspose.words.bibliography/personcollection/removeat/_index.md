---
title: "Aspose::Words::Bibliography::PersonCollection::RemoveAt méthode"
linktitle: "RemoveAt"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Bibliography::PersonCollection::RemoveAt méthode. Supprime la personne à l'index spécifié en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection::RemoveAt method


Supprime la personne à l'index spécifié.

```cpp
void Aspose::Words::Bibliography::PersonCollection::RemoveAt(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | L'index basé sur zéro de la personne à supprimer. |

## Exemples



Montre comment travailler avec la collection de personnes.
```cpp
// Créez une nouvelle collection de personnes.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Ajoutez une nouvelle personne à la collection.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Supprimez la personne de la collection si elle existe.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Créez une collection de personnes avec deux personnes.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Supprimer la personne de la collection par l'index.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Supprimer toutes les personnes de la collection.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Voir aussi

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
