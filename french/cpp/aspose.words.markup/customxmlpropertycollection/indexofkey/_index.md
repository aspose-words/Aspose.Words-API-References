---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection::IndexOfKey méthode"
linktitle: "IndexOfKey"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection::IndexOfKey méthode. Retourne l'index basé sur zéro de la propriété spécifiée dans la collection en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.markup/customxmlpropertycollection/indexofkey/
---
## CustomXmlPropertyCollection::IndexOfKey method


Renvoie l'index basé sur zéro de la propriété spécifiée dans la collection.

```cpp
int32_t Aspose::Words::Markup::CustomXmlPropertyCollection::IndexOfKey(const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom sensible à la casse de la propriété. |

### ReturnValue

L'index basé sur zéro. Valeur négative si non trouvé.

## Exemples



Montre comment travailler avec les propriétés de balises intelligentes pour obtenir des informations détaillées sur les balises intelligentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Une balise intelligente apparaît dans un document lorsque Microsoft Word reconnaît une partie de son texte comme une forme de données,
// telle qu'un nom, une date ou une adresse, et la convertit en hyperlien affichant un soulignement pointillé violet.
// Dans Word 2003, nous pouvons activer les balises intelligentes via "Outils" -> "Options de correction automatique..." -> "SmartTags".
// Dans notre document d'entrée, il y a trois objets que Microsoft Word a enregistrés comme balises intelligentes.
// Les balises intelligentes peuvent être imbriquées, donc cette collection en contient davantage.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// Le membre "Properties" d'une balise intelligente contient ses métadonnées, qui seront différentes pour chaque type de balise intelligente.
// Les propriétés d'une balise intelligente de type "date" contiennent son année, son mois et son jour.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// Nous pouvons également accéder aux propriétés de différentes manières, comme une paire clé-valeur.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Voici trois façons de supprimer des éléments de la collection de propriétés.
// 1 -  Supprimer par indice :
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Videz toute la collection en une fois :
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
