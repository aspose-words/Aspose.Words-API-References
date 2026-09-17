---
title: "Aspose::Words::Fields::DropDownItemCollection::Contains method"
linktitle: "Contains"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::DropDownItemCollection::Contains method. Détermine si la collection contient la valeur spécifiée en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.fields/dropdownitemcollection/contains/
---
## DropDownItemCollection::Contains method


Détermine si la collection contient la valeur spécifiée.

```cpp
bool Aspose::Words::Fields::DropDownItemCollection::Contains(const System::String &value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| value | const System::String\& | Valeur sensible à la casse à localiser. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

## Exemples



Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une zone combinée, puis vérifiez sa collection d'éléments déroulants.
// Dans Microsoft Word, l'utilisateur cliquera sur la zone combinée,
// et choisira ensuite l'un des éléments de texte de la collection à afficher.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Il existe deux façons d'ajouter un nouvel élément à une collection existante d'éléments de boîte déroulante.
// 1 -  Ajouter un élément à la fin de la collection :
dropDownItems->Add(u"Four");

// 2 -  Insérer un élément avant un autre élément à un index spécifié :
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Parcourez la collection et affichez chaque élément.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Il existe deux façons de supprimer des éléments d'une collection d'éléments déroulants.
// 1 -  Supprimer un élément dont le contenu est égal à la chaîne transmise :
dropDownItems->Remove(u"Four");

// 2 -  Supprimer un élément à un index :
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Videz toute la collection d'éléments déroulants.
dropDownItems->Clear();
```

## Voir aussi

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
